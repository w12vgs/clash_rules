# **clash_rules**
---
docker部署订阅转换后台服务  
http://localhost:port/sub  
自定义模板地址填写config.ini的raw地址

# **openclash设置**
---
## 插件设置
**模式设置**  
+ 运行模式:【Fake-IP(TUN-混合)模式】  
+ 网络栈类型：【gVisor】  
&nbsp; 避免网络游戏掉帧卡顿

**DNS设置**  
+  本地 DNS 劫持：【使用Dnsmasq转发】  
+  禁止 Dnsmasq 缓存 DNS 【√】  
###### <font color="red">其他设置随便</font>  

## 覆写设置
**常规设置**
+ URL-Test 策略组切换灵敏度(ms)：【100】
+ 测速（连通性）间隔修改(s)：【180】

 **DNS设置**
+ 自定义上游 DNS 服务器【√】
+ 遵循规则(respect-rules)【×】
+ 追加上游 DNS  【×】
+ 追加默认 DNS 【×】
+ Fake-IP 地址范围 (IPv4 Cidr) 【默认】
+ Fake-IP 持久化 【√】
+ Fallback-Filter 【×】
+ Fake-IP-Filter-Mode 【黑名单模式】
&nbsp;可填写Google应用商店api防止无法Google应用商店无法下载应用
```
#Google应用商店
+.services.googleapis.com
+.xn--ngstr-lra8j.com
```
+ Nameserver-Policy 【√】
+ Hosts 【×】
+ NameServer 【填写自定义DNS地址或本地DNS等】
+ 第三方规则、SOCKS5/HTTP(S) 认证信息留空即可