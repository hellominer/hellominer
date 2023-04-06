<div align="center">

<img src="https://cdn.jsdelivr.net/gh/hellominer/hellominer/docs/logo.png" alt="Logo" width="150" height="150">

<br>

![](https://img.shields.io/static/v1?label=稳&message=原创正版&color=orange)
![](https://img.shields.io/static/v1?label=定&message=稳如老狗&color=blue)
![](https://img.shields.io/static/v1?label=好&message=永不掉线&color=green)
![](https://img.shields.io/static/v1?label=用&message=全币种&color=yellow)

<h3>
    Telegram电报官方群：<a href="https://t.me/hellominer_group">https://t.me/hellominer_group</a>
</h3>
</div>

# hellominer

正版minerproxy专业矿池中转，支持 ETH、ETC、BTC、RVN、ERG、CFX、LTC、XMR、KDA、TON、ALPH、SERO、FIRO、BEAM、ETHW、ETF、FLUX、KAS、HNS、LBC、ZEC、XDAG、DNX，可免费定制，打造专属自己的minerproxy矿池中转，有需要进群找群主。
Web界面操作，简单易用，一键安装，小白可以轻松上手。可以自定义抽水，独创PID抽水算法，稳定精准，秒杀一切市面上随机抽水算法。完美适配各种专业机芯片机。
采用Golang语言开发，性能稳定优异。无视CC，自动CC防护，自动封IP。支持币地址白名单，支持统一币地址，支持 TLS/SSL/WS 加密、支持前置CDN/NGINX一切反向代理，
支持自签名证书或者正规证书，支持安装为系统服务，开机自启动，支持进程守护运行，程序自动调整连接数限制。Telegram交流群 [点击加入](https://t.me/hellominer_group) 。

### 纯转发模式，支持一切币种，支持加密客户端，零损耗，无抽水，零开发费。

## 功能特色

1. 支持主流币种：ETH、ETC、BTC、RVN、ERG、CFX、LTC、XMR、KDA、TON、ALPH、SERO、FIRO、BEAM、ETHW、ETF、FLUX、KAS、HNS、LBC、ZEC、XDAG、DNX，后续支持更多，欢迎进群反馈。
2. 抽水稳定，创新PID算法，不过抽，不少抽，不像市面上所谓的随机方法，抽水不稳定不准确，ETH无损模式。
3. 特有的同池模式，专业机器DAG文件不重新下载，实测完美支持：凤凰ETC芯片机，A11-ETH专业机。
4. 兼容模式，实测支持：神马BTC专业机，蚂蚁E7-BTC专业机。
5. 支持ETH和TON双挖，配置方法欢迎进群咨询。
6. 多种挖矿协议支持，完美支持nicehash，stratum。
7. 无视CC，自动CC防护，自动封IP，还支持手动封IP，解封IP。
8. 支持设置币地址白名单，矿机的提交地址，只有在白名单里面中才能连接中转端口，全方位保护中转服务。
9. 支持统一矿机提交币地址，有效拦截矿机内核抽水。
10. 采用Golang语言开发，网络性能优异。
11. 全部web界面操作，简单易用，小白也能轻松驾驭，同时web界面还适配手机，手机上也能轻松操作。
12. 单机2核，4g，稳定带5000+矿机。
13. 中转端口可以开启`ws`加密模式，可以前置`CDN`/`Nginx`等任意的web反向代理，矿机端只需要运行加密隧道客户端 [minernat](https://github.com/hellominer/minernat) 即可连接`ws`中转端口，全程加密，防止被监控。
14. 中转端口可以开启`ssl/tls`加密模式，配置域名证书和密钥，全程加密，防止被监控。
15. 支持ssl/tls加密协议和tcp协议。
16. 程序支持注册为系统服务，开机自启动，管理端口可以通过配置文件自由修改。
17. 程序还支持手动普通方式运行，此种方式支持`后台守护`参数运行。
18. 程序自动调整ulimit打开文件数限制，无需手动修改系统配置。

## 新增币种

### 没有发现你想要的币种？没关系！如需增加新币种, 请在电报内联系管理员, 通常几个小时就可以完成！

## 系统要求

- 系统类型：Linux: `Debian 9`及以后, `Centos 7`及以后, `Ubuntu 12`及以后。
- 依赖命令：iptables，ipset。
- 一台国外VPS，不要用国内VPS！

## 安装方式

`重要提示：因为会用到iptables，ipset，自动调整系统ulimit连接数限制，所有安装方式都需要root账号权限。`

下面针对不同人群，提供了2种安装方式，选择其中一种进行安装即可。

### 方式一：一键安装

如果是小白，可以执行下面的一键安装脚本，就把hellominer安装为了系统服务。

```shell
bash -c "$(curl -s -L https://github.com/hellominer/hellominer/raw/main/install.sh)" @ install
```

具体程序的`启动`，`停止`，`重启`，`状态`命令如下：

1. 程序启动：`systemctl start hellominer`
2. 程序停止：`systemctl stop hellominer`
3. 程序重启：`systemctl restart hellominer`
4. 程序状态：`systemctl status hellominer`
5. 启动日志：`/etc/hellominer/hellominer logs`
6. 程序卸载：`/etc/hellominer/hellominer uninstall`
7. 程序配置文件路径：`/etc/hellominer/conf`，可以通过修改`/etc/hellominer/conf/app.toml`里面的配置修改程序web管理端口。
8. 默认管理端口是`51301`，假设你的vps的IP是，`192.168.1.1`，那么访问：`http://192.168.1.1:51301` 就可以进入管理登录页面，默认密码是：`123456`。进入后台后，点击右上角头像可以修改密码。

#### 更新程序

更新程序只需要执行：

`
bash -c "$(curl -s -L https://github.com/hellominer/hellominer/raw/main/install.sh)" @ update
`

#### 修改程序配置

hellominer提供了一键配置脚本只需运行：

`
bash -c "$(curl -s -L https://github.com/hellominer/hellominer/raw/main/tools.sh)"
`

### 方式二：手动安装

1. [点击下载 hellominer.tar.gz](https://github.com/hellominer/hellominer/raw/main/releases/hellominer.tar.gz) 。
2. 执行：`mkdir /etc/hellominer`，创建安装目录。
3. 把文件`hellominer.tar.gz`放在目录`/etc/hellominer`下面。
4. 执行：`cd /etc/hellominer && tar zxfv hellominer.tar.gz && ./hellominer init`
5. 执行：`cd /etc/hellominer && ./hellominer` 即可启动，此时是前台运行，关闭ssh后，程序会被关闭，如果一切正常可以加上后台守护参数。
6. 步骤5没问题后，建议后台守护方式运行：`cd /etc/hellominer && ./hellominer --daemon --forever --flog null`
7. 重启程序执行：`pkill hellominer && cd /etc/hellominer && ./hellominer --daemon --forever --flog null`
8. 配置文件目录位于：`/etc/hellominer/conf`,可以通过修改`/etc/hellominer/conf/app.toml`里面的配置，改变程序web管理端口。
9. 默认管理端口是`51301`，假设你的vps的IP是，`192.168.1.1`，那么访问：`http://192.168.1.1:51301` 就可以进入管理登录页面，默认密码是：`123456`
   。进入后台后，点击右上角头像可以修改密码。

#### 更新程序

更新程序只需要复制下面命令执行即可：

`
cd /etc/hellominer && rm -rf hellominer hellominer.tar.gz && curl -o hellominer.tar.gz -s -L https://github.com/hellominer/hellominer/raw/main/releases/hellominer.tar.gz && tar zxfv hellominer.tar.gz
`

更新完毕，需要程序重启，执行：`pkill hellominer && cd /etc/hellominer && ./hellominer --daemon --forever --flog null`


## 使用SSL/TLS加密

### 自定义证书

`hellominer`后台`端口页面`上传自定义证书，端口就使用上传的自定义证书，不需要再手动设置下面的`默认证书`。

### 默认证书

1. 准备证书文件：  
   程序默认自带了自签名证书，位于`/etc/hellominer/conf`目录下面，分别是证书文件`server.crt`和私钥`server.key`,
   如果需要用自己的正规证书，只需要把你的证书改名成`server.crt`，私钥文件改成`server.key`。
   覆盖`/etc/hellominer/conf`目录下面的同名文件即可。

2. 端口启用SSL/TLS加密  
   在添加或者修改矿池页面，本地协议选择`TLS`，`默认证书`即可，然后在首页重载服务，矿机就可以使用SSL加密方式连接此端口了。

## 开启CC防护，认真看第二条！
1. `CC防护`依赖`iptables`和`ipset`命令，确保系统安装了这两个命令
2. `Centos7`及以上版本的系统不再使用`iptables`命令管理防火墙，所以不建议使用`Centos`系统。使用了`Centos`系统开启了`CC防护`导致本软件不能启动，自己解决或者选择其它软件。
3. 推荐 Linux: `Debian 9`及以后, `Ubuntu 12`及以后，执行命令`apt install -y ipset`安装`ipset`。
4. 如果条件1无法满足，切记不能开启CC功能，否则程序无法启动。
5. 修改配置文件：`/etc/hellominer/conf/app.toml`，找到下面这段配置，把`enable = false`改成`enable = true`即可。
   ```ini
   [ccban]
   # enable or disable cc protecting
   enable = true
   ```
1. 修改好配置文件保存，然后重启程序：`systemctl restart hellominer` 即可。

## ETH TON 双挖注意事项
### ETH TON 双挖现已完美支持，但有一定限制.请仔细阅读以下说明并按照要求配置

1.Windows下支持ETH TON双挖的内核有 `teamredminer` [下载地址](https://github.com/todxx/teamredminer/releases/) 请在命令行参数中添加 `--ton_pool_mode=icemining`

2.由于不同TON矿池所用协议不同，目前TON只支持内置的`TON Whales`矿池地址，请勿手动添加其他地址

3.使用双挖时务必将ETH中转模式调整为`兼容模式`！！！

### teamredminer 实例说明：

`teamredminer.exe -a ethash -o stratum+tcp://[ETH中转IP:端口] -u [ETH钱包地址].[矿机名] -p x --ton -o stratum+tcp://[TON中转IP:端口] -u [TON钱包地址].[矿机名] -p x --ton_pool_mode=icemining --ton_end`

注意使用实际真实地址后，不要带[ ]。

## ETH ALPH 双挖注意事项
### ETH ALPH 双挖现已完美支持，请仔细阅读以下说明并按照要求配置。

1.windows 支持 ETH + ALPH 双挖的内核有 `lolminer` [下载地址](https://github.com/Lolliedieb/lolMiner-releases/releases) 。

2.在`hellominer`（假设IP是:`192.168.0.1`）里面添加两个矿池。    
比如：
- ETH 矿池，端口 `1234`，本地端口协议 `TLS`，协议模式：`默认模式`。
- ALPH 矿池，端口 `1235`，本地端口协议 `TLS`，协议模式：`兼容模式`。

3.解压下载的 lolminer 压缩包，用记事本打开解压得到的文件：`dual_mine_eth_aleph_woolypooly.bat`，调整`lolminer`启动参数，修改如下位置的内容。

```text
set "POOL=stratum+tls://192.168.0.1:1234"
set "WALLET=abcd.003"

set "ALEPHPOOL=stratum+tls://192.168.0.1:1235"
set "ALEPHWALLET=defg.003"
```

- 把`192.168.0.1:1234`改成你的 ETH 端口地址，abcd.003改成"你的地址.矿工名"。
- 把`192.168.0.1:1235`改成你的 ALPH 端口地址，defg.003改成"你的地址.矿工名"。

## 使用截图

### 登录页面

![](https://cdn.jsdelivr.net/gh/hellominer/hellominer/docs/login.png)

### 修改密码

![](https://cdn.jsdelivr.net/gh/hellominer/hellominer/docs/changepwd.png)

### 添加矿池

![](https://cdn.jsdelivr.net/gh/hellominer/hellominer/docs/addpool.png)
![](https://cdn.jsdelivr.net/gh/hellominer/hellominer/docs/addpool2.png)

### 添加抽水账号

![](https://cdn.jsdelivr.net/gh/hellominer/hellominer/docs/addaccount.png)

### CC攻击管理

![](https://cdn.jsdelivr.net/gh/hellominer/hellominer/docs/cc.png)

### 端口统计

![](https://cdn.jsdelivr.net/gh/hellominer/hellominer/docs/index.png)

### 纯转发模式

![](https://cdn.jsdelivr.net/gh/hellominer/hellominer/docs/forward1.png)


## 开发抽水比例

```text
根据自定义抽水和矿机情况，0.2% - 0.8% 之间，不是简单阶梯算法较为复杂，不要再试探性的问我抽多少你抽多少。
```

## 问题交流

如果您遇到使用问题，欢迎加入telegram交流群 [点击加入](https://t.me/hellominer_group) 寻求帮助。

## 算力问题
- 首先不明白什么是算力，什么是提交份额的小白，请先补充这方面的知识。
- 其次要明白什么是按着算力百分比抽水，什么是按着提交份额百分比抽水。
- 抽0.1%的份额，需要的算力不是0.1%，它们之间没有一对一的关系，也没一定的公式计算关系。
- 0.1%的份额需要的算力和当前总算力有关，和矿机的算力大小占比有关，一般情况0.1%的份额需要的算力比0.1%算力要大。
- 本软件是抽水是按着份额百分比抽水的，可以精准控制抽水比例。
- 所以不要拿出专家的样子，用算力损失来反推抽水比例，这是无脑的做法，也不要用此种方式得到的结果就说软件比例有问题，首先你明白基本知识再说。

## 测试问题
1. 测试结论和时间，抽水是要时间的，稳定比例也需要时间，着急的`专家`不要上来几分钟，十来分钟，就说这结果不对劲啊？请至少测试1-2小时再看结果情况。
2. 后台的操作包括矿池修改，抽水账号修改后，需要首页`重载服务`才会生效。
3. 矿机登录成功，就被断开，具体表现就是矿机不断的登录成功，成功后立刻被断开,然后要看你的IP是否被监控了，顺便科普一下"监控"，它不是封你的IP，也不是重置你的tcp连接，
   它是发现你的连接发送了挖矿登录的数据包，就会"动作"断开你的tcp，此种情况请你更换IP,或者使用ssl。
4. 矿机直接不能登录，连接超时，应该是IP被屏蔽了，换一个正常IP。
5. 矿机直接不能登录，连接被重置，应该是IP阻断了（换一个正常IP），或者协议不对（使用正确协议）。

## 测试工具

执行下面命令可安装测试工具，验证中转端口是否正常工作。

`curl -o stratum-ping -s -L https://github.com/hellominer/stratum-ping/raw/main/stratum-ping && chmod +x stratum-ping && mv stratum-ping /usr/bin/`

比如你开了中转端口`8080`,IP是`192.168.1.1`，那么执行下面的命令测试端口。

**协议默认模式执行**：

`stratum-ping 192.168.1.1:8080`

**协议兼容模式执行**：

`stratum-ping -t stratum2 192.168.1.1:8080`

## 安全小贴士
1、提供公共中转的老铁们，要知道`币印矿池`，如果矿机通过一个中转入口，中转到你的代理，那么`币印矿池`会把你的中转IP直接显示在矿机使用者的后台，你的中转IP就被暴露出来了，容易受到攻击。

## 更新日志
### v6.0
- 新增纯转发端口模式，支持一切币种，支持加密客户端，零损耗，无抽水，零开发费。

### v5.9
- 更新 DNX 币内置矿池地址。官方关闭了旧的端口，如果旧版本的hellominer无法启用dnx，后台右上角列表点击更新即可。

### v5.8
- 新增 DNX 币代理抽水。

### v5.7
- 新增 XDAG 币代理抽水。

### v5.6
- 新增 ZEC 币代理抽水。

### v5.5
- 新增 HNS、LBC 币代理抽水。

### v5.4
- 新增 KAS 币代理抽水。

### v5.3
- 新增 FLUX 币代理抽水。

### v5.2
- 全面正式支持 ETHW 币代理抽水。
- 现在2miners、f2pool矿池已正式支持 ETHW，交易所欧易支持 ETHW 充提币了，也开启了 ETHW/USDT 交易对。
- 建议所有用户升级。

### v5.1
- 新增 ETHW 币代理抽水，现在k1pool矿池已支持ethw，后面会第一时间增加支持ethw的矿池。
- 新增 ETF 币代理抽水，现在f2pol已支持ETF，后面会第一时间增加支持ETF的矿池。
- 新增代理端口自动压缩传输支持。
- 修复兼容模式stratum不能正常工作的问题。

### v5.0
- 新增 FIRO、BEAM 币抽水代理，它们是 ETH POS 之后的不错的备用选择。
- ETH POS 不慌，有近似替代品即可，hellominer会第一时间支持各种替代币，紧跟潮流，专注稳定，不搞花里胡哨，技术实力雄厚，大家放心使用。

### v4.9
- 新增 SERO 币抽水代理，支持：默认模式（无损），兼容模式，SERO 是 ETH POS 之后的一个备用选择。
- ETH POS 不慌，有近似替代品即可，hellominer会第一时间支持各种替代币，紧跟潮流，技术实力雄厚，大家放心使用。

### v4.8
- 新增后台系统管理，系统日志功能，可以查看关键日志！
- 优化了不会因为当某个币种端口，内置抽水有问题导致软件不能使用的问题。

### v4.7
- 新增 ALPH 币（alephium）抽水代理，显卡机器可以使用lolminer双挖 ETH + ALPH 啦！
- 优化了创建矿池的模式设置，避免了模式和币种关系的误操作。
- 优化了CC屏蔽IP，可以展示时间信息。
- 修复了TON某些情况下的问题。

### v4.6
- 新增币种CFX、KDA支持。
- 优化CC保护策略，默认模式可以精准封掉各种恶意连接和模拟矿机，另外新增严格模式，可以通过配置文件开启严格模式。
- 新增了几个XMR内置地址。

### v4.5
- 新增兼容模式，端口运行期间，客户端数据持久化开关。
- WS/WSS协议，新增自定义底层数据传输数据加密密码设置，留空使用默认，使用WS/WSS加密的好处是，可以从底层协议上彻底杜绝模拟矿机攻击。
- 优化了后台几处存疑的提示。
- 使用了兼容模式的建议升级。

### v4.4
- 新增本地代理端口 WSS 超强加密，可以设置是否发送tls握手域名，穿透力超强，外层tls加密，内层ws双层加密，即使tls中间人探测，也不能突破第二层ws加密。
- 新增矿池配置页面证书设置，可以针对端口设置不同的证书了，也可以选择使用默认证书。

### v4.3
- 修复TRM内核无法使用的问题。
- 新增XMR币支持。

### v4.2
- 新增黑名单机制，可以阻止或者替换黑名单里面的币地址，用于替换内核抽水，或者阻止未知矿机连接。
- 优化矿池列表,矿池新增修改，抽水账号新增修改，均加上了严谨的判断，防止误操作。
- 修复了抽水账号如果配置错误，无法修改的问题。
- 兼容模式新增了抽水算法"准实时模式3"。

### v4.1
- 抽水模式增加到了三种，覆盖了不同显卡机器，不同专业机器，不同币种用到的场景。
- 优化抽水算法，彻底解决在大算力，机器多，抽水比例大的情况下，抽不够的问题。
- ETH/ETC同池模式，新增"印币"支持。
- 修复在线列表某些情况下状态不准确的问题。
- 修复了删除离线机器的有可能不彻底的问题。

### v4.0 重构核心，多协议，多币种支持
- 新增币种ERG，BTC，TON，RVN，LTC挖矿代理和抽水支持。
- 支持ETH和TON双挖，配置方法欢迎进群咨询。
- 新增nicehash协议支持，代理端口新增兼容模式和默认模式，专业机，芯片机全支持。
- 后台操作优化，可以实现端口级别的新增和删除同步服务的新增和删除，避免添加或者删除端口后，重载服务的时候影响其它端口服务。
- 新增首页API功能，外部通过API获取当前首页列表数据。
- 新增集群显示，可以汇总多个hellominer节点首页数据，汇总到一个页面显示。
- 首页列表，多项优化，新增：代理端口，代理模式，协议，币种。
- 抽水力度最大值放开，最大可以达到100。
- 新增抽水模式选择，正常模式（平稳），补偿模式（抽水优先）。

### v3.2
- 后台增加在线升级功能，小白再也不用去ssh登录服务器执行命令升级了。
- CC防护功能，封IP时间调整为永久不过期。
- 优化了CC智能策略，更精准。

### v3.1
- 加入智能CC防御策略，管你什么模拟矿机，肆意TCP连接，通通自动识别，自动封锁恶意IP。
- 后台白名单和统一地址策略调整，开启统一功能，还可以设置白名单作为不统一的地址。
- 提交份额，快速成功回复。
- CC封锁IP数据自动保存，重启程序不丢，重启服务器不丢。
- 修复因为修改了CC封锁时间，程序不能启动的问题。

### v3.0 强势发布
- 重写代理核心代码，采用新算法，矿机稳定长时间在线不掉线，抽水前后矿池本地算力图无损失！
- 监控矿机多久不提交份额，就断开矿机连接，可以在配置文件开启，并配置时间。
- 监控矿机多久不提交算力，就断开矿机，可以在配置文件开启，并配置时间。
- 监控矿机多久没收到矿池任务，就断开矿机，可以在配置文件开启，并配置时间。
- 抽水账号算力图平滑稳定，拜拜心电图！
- 后台矿池开放抽水力度人为调整选项，可以避免过抽或者抽不够的问题！

### v2.6
- 修复抽水账号拒绝过高的问题。

### v2.5
- 新增矿机地址统计，可以发现内核抽水，或者病毒地址。
- 优化抽水，矿池本地算力不丢不抖动。
- 内置矿池地址新增f2pool矿池6个ssl地址。

### v2.4
- 首页新增矿池延迟，移除抽水份额数。
- 优化矿池连接，增加重试，提升稳定性。
- 首页新增矿机地址端口。