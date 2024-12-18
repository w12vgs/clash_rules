
## openclash设置
---
## 插件设置
**模式设置**  
+ 运行模式:【Fake-IP(TUN-混合)模式】  
+ 网络栈类型：【gVisor】  
&nbsp; 避免网络游戏掉帧卡顿

**DNS设置**  
+  本地 DNS 劫持：【使用Dnsmasq转发】  
+  禁止 Dnsmasq 缓存 DNS 【√】  

```diff
- 其他设置随便
```
## 覆写设置

**常规设置**
+ URL-Test 策略组切换灵敏度(ms)：【100】
+ 测速（连通性）间隔修改(s)：【180】

**DNS 设置**
+ 自定义上游 DNS 服务器【√】
+ 遵循规则(respect-rules)【□】
+ 追加上游 DNS  【□】
+ 追加默认 DNS 【□】
+ Fake-IP 地址范围 (IPv4 Cidr) 【默认】
+ Fake-IP 持久化 【√】
+ Fallback-Filter 【□】
+ Fake-IP-Filter-Mode 【黑名单模式】
&nbsp;可填写Google应用商店api防止无法Google应用商店无法下载应用
```
#Google应用商店
+.services.googleapis.com
+.xn--ngstr-lra8j.com
```
+ Nameserver-Policy 【√】
+ Hosts 【□】
+ NameServer 【填写自定义DNS地址或本地DNS等】

**Meta 设置**
+ 启用 TCP 并发 【√】
+ 启用统一延迟 【√】
+ 启用进程规则 【禁用】
+ 客户端指纹 【禁用】
+ Geodata 数据加载方式 【小内存模式】
+ 启用 GeoIP Dat 版数据库 【□】
+ 启用流量（域名）探测 【√】
+ 探测（嗅探）纯 IP 连接【√】
+ 自定义流量探测（嗅探）设置 【□】

```diff  
- 其他设置随便</font> 
```

## 配置订阅
前置任务（或者直接使用别人的在线后台）
**docker部署订阅转换后台服务** 
```
version: "3.3"
services:
  subconverter:
    restart: always
    ports:
      - 25500:25500
    image: tindy2013/subconverter:latest
networks: {}
```

http://localhost:port/sub  
自定义模板地址填写**config.ini**的Raw地址