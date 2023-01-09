# HTTP版本
## HTTP/1.0
HTTP 正式作为标准被公布是在 1996 年的 5 月，版本被命名为 HTTP/1.0，并记载于 RFC1945。虽说是初期标准，但该协议标准至今仍 被广泛使用在服务器端。  
https://www.ietf.org/rfc/rfc1945.txt
## HTTP/1.1
1997 年 1 月公布的 HTTP/1.1 是目前主流的 HTTP 协议版本。当初 的标准是 RFC2068，之后发布的修订版 RFC2616 就是当前最广泛使用的版本。
https://www.ietf.org/rfc/rfc2616.txt
## HTTP/2.0
2015年HTTP/2.0正式发表。
https://www.ietf.org/rfc/rfc7540.txt
# TCP/IP协议族
与互联网相关联的协议集合起来总称为TCP/IP。
网络是在TCP/IP协议族的基础上运作的，而HTTP属于它的一个子集。
## TCP/IP的分层
### 应用层
各类通用的应用服务。
如 FTP、DNS、HTTP。
### 传输层
传输层对上层应用层，提供处于网络连接中的两台计算机之间的数据传输。
 如 TCP（Transmission Control Protocol，传输控制协议）和 UDP（User Data Protocol，用户数据 报协议）
### 网络层
网络层用来处理在网络上流动的数据包。数据包是网络传输的最小数据单位。该层规定了通过怎样的路径（所谓的传输路线）到达对方计算机，并把数据包传送给对方。  
### 链路层
 用来处理连接网络的硬件部分。
## TCP/IP通信传输流
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673157649634-65e31c47-9623-4562-b008-6dadf767459b.png#averageHue=%23c5b990&clientId=u32997a6a-1889-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=704&id=uac9d5476&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1056&originWidth=1192&originalType=binary&ratio=1&rotation=0&showTitle=false&size=118114&status=done&style=none&taskId=ufdcaf5b4-8720-4b93-895f-3b38dd461f3&title=&width=794.6666666666666)

这种把数据包装起来的做法叫做**封装**。
# IP协议
IP实际上指IP协议的名称，注意不要搞混IP和IP地址。
IP协议的作用是把各种数据包传送给对方。而要保证确实传送到对方那里，则需要满足各类条件。其中两个重要的条件是 **IP 地址**和 **MAC 地址**（Media Access Control Address） 
IP 地址指明了节点被分配到的地址，MAC 地址是指网卡所属的固定地址。IP 地址可以和 MAC 地址进行配对。IP 地址**可变换**，但 MAC 地址**基本上不会更改**。 
# ARP协议
IP 间的通信依赖 MAC 地址。在网络上，通信的双方在同一局域网 （LAN）内的情况是很少的，通常是经过多台计算机和网络设备中转才 能连接到对方。而在进行中转时，会利用下一站中转设备的 MAC 地址来搜索下一个中转目标。这时，会采用 **ARP 协议**（Address Resolution Protocol）。ARP 是一种用以解析地址的协议，根据通信方的 IP 地址就可以反查出对应的 MAC 地址。 
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673158833602-f19296ab-8ed4-4838-aa0b-c136edea4f14.png#averageHue=%23fdfcfc&clientId=u32997a6a-1889-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=726&id=u4f620d9d&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1089&originWidth=1269&originalType=binary&ratio=1&rotation=0&showTitle=false&size=372941&status=done&style=none&taskId=ub5293f37-9cbb-45fe-a792-6508becfc2c&title=&width=846)
# TCP协议
 TCP 位于传输层，提供可靠的字节流服务。
**字节流服务**是指，为了方便传输， 将大块数据**分割**成以报文段（segment）为单位的**数据包**进行管理。TCP 协议为了更容易传送大数据才把数据分割，而且 TCP 协议能够确认数据最终是否送达到对方。 
为了准确无误地将数据送达目标处，TCP 协议采用了三次握手策略 
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673159081931-37fffd3e-1347-4e02-b541-391245042878.png#averageHue=%23fdfdfc&clientId=u32997a6a-1889-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=441&id=u6d57fe6c&margin=%5Bobject%20Object%5D&name=image.png&originHeight=661&originWidth=1214&originalType=binary&ratio=1&rotation=0&showTitle=false&size=231695&status=done&style=none&taskId=u9fe0e3a0-b141-40fa-820d-04406d5ca7c&title=&width=809.3333333333334)
若在握手过程中某个阶段莫名中断，TCP 协议会再次以相同的顺序发送相同的数据包。
# DNS协议
DNS 协议提供通过域名查找 IP 地址，或逆向从 IP 地址反查域名的服务。 
# 各协议与HTTP的关系
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673159364800-f9a3b663-a56c-41c2-a197-40649e883d7b.png#averageHue=%23fcfbfa&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=925&id=u020f2e43&margin=%5Bobject%20Object%5D&name=image.png&originHeight=966&originWidth=654&originalType=binary&ratio=1&rotation=0&showTitle=false&size=207969&status=done&style=none&taskId=ua4e7d0e1-1c40-4422-920d-6295848f214&title=&width=626)
# URL和URI
URI（ Uniform Resource Identifier  统一资源标识符） 
URL （Uniform Resource Locator 统一资源定位符）  
其中URI包含URL
## URI格式
绝对URI的格式如下
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673159918341-7a44606f-0f20-4d76-8a23-0f50dbb4e952.png#averageHue=%23fcfaf8&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=125&id=u5e7b0c91&margin=%5Bobject%20Object%5D&name=image.png&originHeight=184&originWidth=928&originalType=binary&ratio=1&rotation=0&showTitle=false&size=51692&status=done&style=none&taskId=u74dc285f-d3e8-407c-a57a-fa4d3e1f2a1&title=&width=631.6666870117188)
# HTTP中的方法
## GET
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673160695782-cb8b6783-1f49-4606-95ea-61483838887d.png#averageHue=%23fdfdfd&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=223&id=u9b8d91f0&margin=%5Bobject%20Object%5D&name=image.png&originHeight=335&originWidth=885&originalType=binary&ratio=1&rotation=0&showTitle=false&size=84024&status=done&style=none&taskId=u31e7e375-6323-4e18-b60b-46c46dd6996&title=&width=590)
## POST
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673160704946-3a25c163-622c-4739-979e-e4ec0e483c20.png#averageHue=%23fdfdfd&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=225&id=u87df6763&margin=%5Bobject%20Object%5D&name=image.png&originHeight=338&originWidth=914&originalType=binary&ratio=1&rotation=0&showTitle=false&size=85182&status=done&style=none&taskId=ufe6d3fbd-a1ef-4d09-a3ce-25430790d71&title=&width=609.3333333333334)
## PUT
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673160714886-fbc5e176-1018-4b22-96f5-6a2208880120.png#averageHue=%23fdfdfd&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=213&id=u5ed95862&margin=%5Bobject%20Object%5D&name=image.png&originHeight=320&originWidth=884&originalType=binary&ratio=1&rotation=0&showTitle=false&size=87620&status=done&style=none&taskId=u93bad453-a513-4975-a7f7-709fc81e6e7&title=&width=589.3333333333334)
## HEAD
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673160728186-a0a4da47-0cdd-464f-bd98-37f4a71b4aeb.png#averageHue=%23fefdfd&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=243&id=u9ce446a2&margin=%5Bobject%20Object%5D&name=image.png&originHeight=364&originWidth=916&originalType=binary&ratio=1&rotation=0&showTitle=false&size=88124&status=done&style=none&taskId=ud81898f8-6ee7-4712-8905-b64f572e739&title=&width=610.6666666666666)
## DELETE
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673160741619-9ee59ae6-2680-4053-8f4f-05f2bcc9f699.png#averageHue=%23fdfdfd&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=213&id=u95249674&margin=%5Bobject%20Object%5D&name=image.png&originHeight=320&originWidth=878&originalType=binary&ratio=1&rotation=0&showTitle=false&size=93912&status=done&style=none&taskId=u7e12b661-7b1c-4f12-8d89-3cd35ec00ca&title=&width=585.3333333333334)
## OPTIONS
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673160750706-fb50c57e-4560-4d8b-9cd1-a3f7946448ce.png#averageHue=%23fdfdfd&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=213&id=u67491c9e&margin=%5Bobject%20Object%5D&name=image.png&originHeight=320&originWidth=1001&originalType=binary&ratio=1&rotation=0&showTitle=false&size=99918&status=done&style=none&taskId=u5fb249c7-f3e0-492d-a6ac-1e769001f22&title=&width=667.3333333333334)
## TRACE
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673160781535-2dc3ad79-2dd5-4a9c-8eba-bf95c0cff1f2.png#averageHue=%23fcfbfb&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=263&id=u67c70893&margin=%5Bobject%20Object%5D&name=image.png&originHeight=394&originWidth=1037&originalType=binary&ratio=1&rotation=0&showTitle=false&size=196146&status=done&style=none&taskId=u3e523aa2-023d-430b-ad3c-6fa19d182d2&title=&width=691.3333333333334)
## CONNECT
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673160790913-2e822b28-39d1-4ed5-92ed-2b6a4b1af431.png#averageHue=%23cdb397&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=236&id=u410964c9&margin=%5Bobject%20Object%5D&name=image.png&originHeight=354&originWidth=1013&originalType=binary&ratio=1&rotation=0&showTitle=false&size=143449&status=done&style=none&taskId=ue64445f0-e75a-4f0c-acb1-193227b9e4a&title=&width=675.3333333333334)
CONNECT 方法要求在与代理服务器通信时建立隧道，实现用隧道协议进行 TCP 通信。主要使用 SSL（Secure Sockets Layer，安全套接 层）和 TLS（Transport Layer Security，传输层安全）协议把通信内容加密后经网络隧道传输 。
# 持久连接
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673160962789-7f3e5fbf-6c8d-4d00-9401-ce72cb894a59.png#averageHue=%23bda27d&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=541&id=u3fc35fb1&margin=%5Bobject%20Object%5D&name=image.png&originHeight=812&originWidth=1055&originalType=binary&ratio=1&rotation=0&showTitle=false&size=179936&status=done&style=none&taskId=ua251f7f8-41a5-4e41-a225-9772f18324b&title=&width=703.3333333333334)
# 管线化
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673161038631-9a7cccc0-6170-4992-a342-5dba58a601b9.png#averageHue=%23ccb28d&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=319&id=u6af808a8&margin=%5Bobject%20Object%5D&name=image.png&originHeight=478&originWidth=1017&originalType=binary&ratio=1&rotation=0&showTitle=false&size=147506&status=done&style=none&taskId=u5a1d83dc-d017-4cc4-b608-8a2083481f3&title=&width=678)
# Cookie
Cookie会根据从服务器端发送的响应报文内的一个叫做 Set-Cookie 的首部字段信息，通知客户端保存 Cookie。当下次客户端再往该服务器 发送请求时，客户端会自动在请求报文中加入 Cookie 值后发送出去。  
服务器端发现客户端发送过来的 Cookie 后，会去检查究竟是从哪一个客户端发来的连接请求，然后对比服务器上的记录，最后得到之前的状态信息。  
# HTTP报文
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673161365382-c42c9d06-bebf-46e2-87f3-1b33eaa9710a.png#averageHue=%23d1b48e&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=229&id=u0e9069b5&margin=%5Bobject%20Object%5D&name=image.png&originHeight=343&originWidth=1051&originalType=binary&ratio=1&rotation=0&showTitle=false&size=79567&status=done&style=none&taskId=u6b57d926-2e42-4d12-b7ea-0fe2b41a468&title=&width=700.6666666666666)
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673161485453-8bdeff9d-e95d-406a-8998-caf9df75ffca.png#averageHue=%23a0c0a2&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=153&id=ua8fe2c7f&margin=%5Bobject%20Object%5D&name=image.png&originHeight=230&originWidth=1016&originalType=binary&ratio=1&rotation=0&showTitle=false&size=34202&status=done&style=none&taskId=u469e2410-1f12-44a2-b47f-61291cb923f&title=&width=677.3333333333334)
## 请求行
包含用于请求的方法，请求 URI 和 HTTP 版本。 
## 状态行
包含表明响应结果的状态码，原因短语和 HTTP 版本。  
## 首部字段
包含表示请求和响应的各种条件和属性的各类首部。
# 范围请求
执行范围请求时，会用到首部字段 Range 来指定资源的 byte 范围。 byte 范围的指定形式如下。  
```
//5001~10 000 字节
Range: bytes=5001-10000 
//从 5001 字节之后全部的
Range: bytes=5001-
//从一开始到 3000 字节和 5000~7000 字节的多重范围
Range: bytes=-3000, 5000-7000
```
针对范围请求，响应会返回状态码为 206 Partial Content 的响应报 文。另外，对于多重范围的范围请求，响应会在首部字段 Content-Type 标明 multipart/byteranges 后返回响应报文。 如果服务器端无法响应范围请求，则会返回状态码 200 OK 和完整 的实体内容 。
# 状态码
|  1XX |  Informational（信息性状态码）   |  接收的请求正在处理   |
| --- | --- | --- |
|  2XX |  Success（成功状态码）   |  请求正常处理完毕   |
|  3XX |  Redirection（重定向状态码）   |  需要进行附加操作以完成请求   |
|  4XX |  Client Error（客户端错误状态码）   |  服务器无法处理请求   |
|  5XX |  Server Error（服务器错误状态码）   |  服务器处理请求出错   |

## 200 OK
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673162565201-8394f397-8bc8-4317-984e-06ddd133cf3a.png#averageHue=%23fdfcfc&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=201&id=u060c4390&margin=%5Bobject%20Object%5D&name=image.png&originHeight=301&originWidth=938&originalType=binary&ratio=1&rotation=0&showTitle=false&size=107549&status=done&style=none&taskId=u9b745166-0404-4bce-ad8e-30d9f47e352&title=&width=625.3333333333334)
## 204 No content
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673162576598-9eda4176-61be-4ba7-9f75-435ce0958640.png#averageHue=%23fdfcfc&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=202&id=u8adcfd2f&margin=%5Bobject%20Object%5D&name=image.png&originHeight=303&originWidth=867&originalType=binary&ratio=1&rotation=0&showTitle=false&size=94033&status=done&style=none&taskId=ud08825df-6ec3-4fd0-b5b7-6b01082dacb&title=&width=578)
## 206 Partial Content  
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673162647501-8b21b61a-059b-46ee-bb32-8bef8d146581.png#averageHue=%23fcfcfc&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=194&id=ube6c5941&margin=%5Bobject%20Object%5D&name=image.png&originHeight=291&originWidth=869&originalType=binary&ratio=1&rotation=0&showTitle=false&size=100971&status=done&style=none&taskId=u69ad21e9-3d86-40bc-b6ec-1e82885d8a8&title=&width=579.3333333333334)
## 301 Moved Permanently  
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673162691255-45b21454-b7bf-4dd4-b317-7c196410447e.png#averageHue=%23fdfcfc&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=211&id=ud442b13c&margin=%5Bobject%20Object%5D&name=image.png&originHeight=317&originWidth=920&originalType=binary&ratio=1&rotation=0&showTitle=false&size=110635&status=done&style=none&taskId=u9730727f-08e9-4044-a517-d85932e48bc&title=&width=613.3333333333334)
## 302 Found
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673162796087-b59c688c-e58b-4d8d-82a2-73356a758ff5.png#averageHue=%23fdfcfc&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=248&id=ua783ff79&margin=%5Bobject%20Object%5D&name=image.png&originHeight=372&originWidth=899&originalType=binary&ratio=1&rotation=0&showTitle=false&size=110394&status=done&style=none&taskId=u4075d13a-d280-4438-ae91-e75d1ede8ea&title=&width=599.3333333333334)
## 303 See other
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673162865830-b763e89f-c69f-4567-bbef-543815bf558c.png#averageHue=%23fdfcfc&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=242&id=u91074649&margin=%5Bobject%20Object%5D&name=image.png&originHeight=363&originWidth=842&originalType=binary&ratio=1&rotation=0&showTitle=false&size=105842&status=done&style=none&taskId=u0bee592a-30db-419d-b823-5b8a5536d84&title=&width=561.3333333333334)
303 状态码和 302 Found 状态码有着相同的功能，但 303 状态码明确表示客户端应当采用 GET 方法获取资源，这点与 302 状态码有区别。  
## 304 Not Modified
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673162958764-822cdc8e-4091-4bb0-922c-28fc8832e75b.png#averageHue=%23fdfdfc&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=238&id=u1fd96773&margin=%5Bobject%20Object%5D&name=image.png&originHeight=357&originWidth=871&originalType=binary&ratio=1&rotation=0&showTitle=false&size=101577&status=done&style=none&taskId=u54c0f75e-034a-4921-863f-51348982813&title=&width=580.6666666666666)
## 307 Temporary Redirect  
临时重定向。该状态码与 302 Found 有着相同的含义。尽管 302 标 准禁止 POST 变换成 GET，但实际使用时大家并不遵守 。
## 400 Bad Request  
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673163056382-afa03cde-887b-4f1f-87dd-855381564681.png#averageHue=%23fdfdfc&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=211&id=u15fb3c9f&margin=%5Bobject%20Object%5D&name=image.png&originHeight=317&originWidth=809&originalType=binary&ratio=1&rotation=0&showTitle=false&size=93441&status=done&style=none&taskId=u4ab9f1af-a3c8-4951-a900-14f9d4bc933&title=&width=539.3333333333334)
## 401 Unauthorized  
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673163099589-171954fd-a034-497a-9756-dd7269b0a122.png#averageHue=%23c5b690&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=452&id=ud77b12af&margin=%5Bobject%20Object%5D&name=image.png&originHeight=678&originWidth=770&originalType=binary&ratio=1&rotation=0&showTitle=false&size=168888&status=done&style=none&taskId=u309087b7-fab9-42ed-885f-43aba9c233c&title=&width=513.3333333333334)
## 403 Forbidden  
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673163157171-c5b1b836-2164-4ad6-a04f-d8639903c0d0.png#averageHue=%23fdfdfc&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=209&id=u4786e11a&margin=%5Bobject%20Object%5D&name=image.png&originHeight=314&originWidth=836&originalType=binary&ratio=1&rotation=0&showTitle=false&size=89535&status=done&style=none&taskId=u7e119c1b-039b-4587-874c-3d5b27166df&title=&width=557.3333333333334)
## 404 Not Found 
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673163198268-7bf8c8c4-b825-4874-9bfb-bf1401e57ab8.png#averageHue=%23cecaa2&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=239&id=u1f4b21b9&margin=%5Bobject%20Object%5D&name=image.png&originHeight=358&originWidth=1015&originalType=binary&ratio=1&rotation=0&showTitle=false&size=75206&status=done&style=none&taskId=uf0ef2a63-bc5a-4d29-9710-c858c5f49af&title=&width=676.6666666666666)
 该状态码表明服务器上无法找到请求的资源。除此之外，也可以在 服务器端拒绝请求且不想说明理由时使用。 
## 500 Internal Server Error  
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673163266674-4d1e3d41-7ae7-4f92-b7e7-4a38d55fc5c7.png#averageHue=%23fdfdfc&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=212&id=ue998a3d2&margin=%5Bobject%20Object%5D&name=image.png&originHeight=318&originWidth=842&originalType=binary&ratio=1&rotation=0&showTitle=false&size=90991&status=done&style=none&taskId=u19becc50-0f3f-42f5-9b84-96480ff4f4a&title=&width=561.3333333333334)
## 503 Service Unavailable  
![image.png](https://cdn.nlark.com/yuque/0/2023/png/34003712/1673163290043-ab166945-653f-46cf-8172-9b18505484be.png#averageHue=%23fdfdfd&clientId=u528a9ada-2469-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=223&id=u3cb151c1&margin=%5Bobject%20Object%5D&name=image.png&originHeight=334&originWidth=864&originalType=binary&ratio=1&rotation=0&showTitle=false&size=87955&status=done&style=none&taskId=uc31d897d-dc6c-442b-8ec8-36783e83813&title=&width=576)
# HTTPS
HTTPS 并非是应用层的一种新协议。只是 HTTP 通信接口部分用 SSL（Secure Socket Layer）和 TLS（Transport Layer Security）协议代替而已。

