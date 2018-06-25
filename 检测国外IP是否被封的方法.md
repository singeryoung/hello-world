# IP 是否被封
在判断是否 Ping 的前提下还要判断端口是否被封，两者兼顾的情况下才可以判断出 IP 是否被封。 

## 一、国内外 Ping 测试
当IP无法Ping通时主要表现形式有以下三种：
1、国内可Ping通，国外也可Ping通；
2、国内无法Ping通，国外可Ping通；
3、国内无法Ping通，国外也无法Ping通.（两种可能：VPS配置禁Ping或者VPS停止运行）

访问网站https://www.ipip.net/ping.php
国内多个地点ping http://ping.chinaz.com/

如果国内无法 Ping 国外可以 Ping，那么此 IP 一定是被封了，换 IP 吧；而如果国内外都可以 Ping，那么此时就无法判断出是否已经被封了，还需要进行下一步端口扫描测试。

## 二、国内外端口扫描测试
### 1、国内测试
国内端口扫描站（http://tool.chinaz.com/port）
### 2、国外测试
国外端口扫描站（https://www.yougetsignal.com/tools/open-ports/）

如果显示此 SSH 连接端口为开启状态，加上前面检测到的此 SSH 连接端口在国内为关闭状态，此时完全可以确定此 IP 已经被封！而如果显示此 SSH 连接端口依旧为关闭状态，那么就检查下机器是不是在正常运行以及端口是否填写错误。

引用链接：
https://www.banwagongzw.com/72.html
https://www.banwagongzw.com/31.html
