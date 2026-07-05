# 搬瓦工 KiwiVM 软件下载完整指南：KiwiVM 到底装不装？怎么打开控制面板？手机能用吗？登录失败怎么办？（附最新套餐对比）

搜"搬瓦工 KiwiVM 软件下载"的人，基本上踩了同一个坑。

我第一次用搬瓦工的时候也这样——买完 VPS，到处找 KiwiVM 的安装包，找不到，以为是官网没放出来，翻了半天才搞明白：**KiwiVM 根本不需要下载**。它是一个网页版控制面板，你的浏览器就是"软件"，买了搬瓦工的账号，直接在网页里登进去就能用，没有 exe，没有 dmg，什么都没有。

说清楚这一点，才能往下说怎么用。

---

## 什么是 KiwiVM？为什么搜索"KiwiVM 下载"会找不到

KiwiVM Control Panel 是搬瓦工（BandwagonHost）自己开发的 VPS 管理面板，每买一台搬瓦工 VPS，就会对应一个独立的 KiwiVM 实例。

它能做的事情比较多：

- 查看 VPS 的 IP 地址、SSH 端口、流量用量
- 开机、关机、强制重启
- 一键重装系统（支持多个 Linux 发行版，Ubuntu、Debian、Rocky Linux 等）
- 迁移机房（搬瓦工支持在多个数据中心之间自由切换，不扣流量）
- 修改 root 密码、修改 KiwiVM 面板密码
- 创建/下载/还原快照（快照功能免费）
- 在线 VNC / 基础 Shell 控制台
- 查看 API Key，供第三方调用

说实话，这套面板的 UI 不算好看，功能排列也不算直观。但用了一段时间之后还是觉得够用——该有的都有，迁移机房这个功能尤其实用，网速不好的时候直接换个机房，不用重新买。

所以回到开头的问题：KiwiVM 软件下载 = 没有独立软件可以下载，它就是个网页面板。

👉 [去搬瓦工购买 VPS，获取 KiwiVM 控制面板访问权限](https://bit.ly/BanWaGon)

---

## 如何打开 KiwiVM 控制面板：两种方式

买完套餐之后，进入 KiwiVM 有两个入口，选一个用就行。

### 方式一：从搬瓦工账号后台进入（推荐新手）

1. 登录搬瓦工账号后台（Client Area）
2. 点击右上角的 **Services → My Services**
3. 找到你购买的 VPS，点击后方的 **KiwiVM Control Panel** 按钮
4. 自动跳转并登录到 KiwiVM 面板

这个方式不需要记任何额外密码，点一下就进去了，适合刚买的新用户。

### 方式二：直接访问 KiwiVM 地址登录

KiwiVM 面板有一个独立的登录地址，用 VPS 的 IP 地址 + KiwiVM 专属密码登录。

这个密码跟你的搬瓦工账号密码不是同一个，也跟 root 密码不一样——是第三个独立的密码。如果你不知道这个密码是多少，用方式一进去之后，在面板里找 **KiwiVM password modification** 重置一下。

---

## KiwiVM 面板各功能在哪里

进了面板之后，左侧是功能导航，分三个大区：

**Admin functions（主要管理功能）**

- Main Controls：VPS 状态、开关机、基本信息一览
- Install new OS：重装系统，下拉选版本，点一下就开始装
- Root password modification：改 root 密码
- KiwiVM password modification：改面板登录密码
- Two-factor authentication：开启二步验证，建议打开
- Detailed statistics：流量、CPU、带宽的详细统计图
- Snapshots：快照管理，备份和恢复
- Audit log：操作记录，查最近做了什么

**Migration（机房迁移）**

- Migrate to another DC：选目标机房，一键迁过去，不收费，次数不限，数据保留

**KiwiVM Extras（额外功能）**

- Root Shell (Basic / Advanced / Interactive)：在浏览器里直接执行命令，不开 SSH 客户端也能凑合用
- VNC：图形化控制台，SSH 挂了的时候应急用
- API：查看 VEID 和 API Key，用来对接第三方脚本或管理工具

---

## 手机上怎么管理搬瓦工 VPS？

KiwiVM 是网页面板，手机上用浏览器也能打开，但布局是桌面版的，操作起来不太方便，字小、按钮密。

好消息是搬瓦工提供了官方 API 接口，开发者可以通过 API 调用来管理 VPS。你需要的是：进 KiwiVM 面板，找到 **API** 选项，记下 **VEID** 和 **API KEY** 这两个值。有了这两个值，配合支持搬瓦工 API 的第三方工具，就能在手机上控制 VPS 的基本操作（重启、停止、查状态等）。

顺便说一句，进 KiwiVM 面板偶尔会看到 **Session Expired** 提示，清一下浏览器 Cookie 就好了，不是账号出问题。

---

## 搬瓦工套餐选哪个：KiwiVM 功能一样，区别在线路和机房

KiwiVM 面板所有套餐都有，功能没有区别。套餐之间的差异主要是线路、机房、配置和价格。

下面是目前搬瓦工官网在售的主要套餐：

| 套餐系列 | 内存 | CPU | 硬盘 | 月流量 | 带宽 | 可选机房 | 价格 | 购买 |
|---|---|---|---|---|---|---|---|---|
| KVM 入门款 | 1GB | 2核 | 20GB SSD | 1TB | 1Gbps | DC2 QNET、DC8 ZNET 等欧美多机房 | $49.99/年 |  [选择此方案](https://bandwagonhost.com/aff.php?aff=80238&pid=44) |
| KVM 标准款 | 2GB | 3核 | 40GB SSD | 2TB | 1Gbps | 欧美多机房 | $99.99/年 |  [选择此方案](https://bandwagonhost.com/aff.php?aff=80238&pid=45) |
| CN2 套餐 入门 | 1GB | 1核 | 20GB SSD | 1TB | 1Gbps | DC3 CN2 为主，可选多机房 | $49.99/年 |  [选择此方案](https://bandwagonhost.com/aff.php?aff=80238&pid=57) |
| CN2 套餐 标准 | 2GB | 1核 | 40GB SSD | 2TB | 1Gbps | 同上 | $99.99/年 |  [选择此方案](https://bandwagonhost.com/aff.php?aff=80238&pid=58) |
| **CN2 GIA-E（最推荐）** | 1GB | 2核 | 20GB SSD | 1TB | 2.5Gbps | DC6 CN2 GIA-E、DC9 CN2 GIA、日本软银、荷兰联通等 12 个机房 | $49.99/季 / $169.99/年 |  [选择此方案](https://bandwagonhost.com/aff.php?aff=80238&pid=87) |
| CN2 GIA-E 大流量 | 2GB | 3核 | 40GB SSD | 2TB | 2.5Gbps | 同上 12 个机房 | $89.99/季 / $299.99/年 |  [选择此方案](https://bandwagonhost.com/aff.php?aff=80238&pid=88) |
| 香港 CN2 GIA 小套餐 | 2GB | 2核 | 40GB SSD | 500GB | 1Gbps | 中国香港 CN2 GIA | $89.99/月 / $899.99/年 |  [选择此方案](https://bandwagonhost.com/aff.php?aff=80238&pid=95) |
| 香港 CN2 GIA 大套餐 | 4GB | 4核 | 80GB SSD | 1TB | 1Gbps | 中国香港 CN2 GIA | $155.99/月 / $1559.99/年 |  [选择此方案](https://bandwagonhost.com/aff.php?aff=80238&pid=96) |
| 日本大阪 CN2 GIA 小 | 2GB | 2核 | 40GB SSD | 500GB | 1.5Gbps | 日本大阪 CN2 GIA | $49.99/月 / $499.99/年 |  [选择此方案](https://bandwagonhost.com/aff.php?aff=80238&pid=134) |
| 日本大阪 CN2 GIA 大 | 4GB | 4核 | 80GB SSD | 1TB | 1.5Gbps | 日本大阪 CN2 GIA | $86.99/月 / $869.99/年 |  [选择此方案](https://bandwagonhost.com/aff.php?aff=80238&pid=135) |

几句话帮你选：

- **学 Linux / 搭个小站 / 预算有限** → 入门 KVM $49.99/年，够了，用着看看感觉
- **国内访问速度要求一般** → CN2 套餐 $49.99/年，比 KVM 线路稍好一点
- **想要速度还要省钱** → CN2 GIA-E $169.99/年，性价比在整个套餐里算最高的，还能在 12 个机房来回切换找最优延迟
- **追求极低延迟、不在意价格** → 香港 CN2 GIA，贵但延迟确实低，广东方向体感明显

支付方式支持支付宝，不需要信用卡，结算页直接选就行。

---

## KiwiVM 常见操作：新手必知的几件事

**重装系统**

进 KiwiVM 后找 Install new OS，选你要的系统版本，点 Reload。一般 5 分钟内完成，重装后 root 密码会发到注册邮箱，记得去查。

**迁移机房**

左侧菜单找 Migrate to another DC，选目标机房，确认就开始迁。数据带走，IP 会换，迁移时间一般十几分钟。如果当前机房速度变慢或者延迟变高，可以试试换一个。CN2 GIA-E 套餐最大好处是可以在 12 个机房里自由挑，别的套餐机房选项少一点。

**修改 root 密码**

Root password modification 里操作，改完之后要重启 VPS 才生效。

**开启二步验证**

Two-factor authentication 里开，需要配合 Google Authenticator 或者 Authy 这类软件生成验证码。开了之后每次登 KiwiVM 多输一个动态码，安全性高一截。实测用下来没什么麻烦，建议直接开。

---

## 用下来的感受

KiwiVM 面板用了几年，习惯了就好，最常用的功能其实就三个：查流量用了多少、重装系统、迁机房。快照功能偶尔用，做完重要配置之前先打个快照，心里踏实。

稳定性这块没遇到过大问题。偶尔一两次 Session Expired，清 Cookie 就好了。面板本身不会成为你管理 VPS 的瓶颈。

30 天内不满意可以全额退款，第一次买不确定的话可以先试试入门款，不合适直接退。

👉 [查看搬瓦工当前所有套餐与最新价格](https://bit.ly/BanWaGon)

---

## 常见问题

**Q：KiwiVM 是免费的吗？**

KiwiVM 控制面板是搬瓦工 VPS 自带的，买了 VPS 就有，不需要额外付费。

**Q：KiwiVM 软件怎么下载到电脑上？**

不需要下载。KiwiVM 是网页控制面板，用浏览器打开就能用。登录入口在搬瓦工账号后台的 Services → My Services 里。

**Q：KiwiVM 面板忘记密码怎么办？**

KiwiVM 面板有独立密码，和账号密码、root 密码都不同。可以先从搬瓦工账号后台点击 KiwiVM Control Panel 按钮直接跳转进去（不需要输面板密码），进去之后再在 KiwiVM password modification 里重置。

**Q：搬瓦工 VPS 支持安装 Windows 吗？**

支持，KiwiVM 面板的 Install new OS 里有 Windows 10 的选项，需要通过挂载 ISO 镜像方式安装。不过搬瓦工 VPS 跑 Windows 比较费资源，一般不推荐，用 Linux 更顺。

**Q：搬瓦工套餐买完之后还可以换机房吗？**

可以，CN2 GIA-E 套餐支持在 12 个机房之间自由迁移，免费不限次数。其他套餐也支持迁移，但可选机房数量少一些，具体看套餐说明。

**Q：KiwiVM 里的 API Key 有什么用？**

API Key 配合 VEID 可以通过代码或脚本调用搬瓦工 VPS 的管理接口，做自动重启、状态监控、迁机房等操作，不用每次手动登面板。对需要自动化管理的用户比较有用。

---

👉 [前往搬瓦工获取最适合你的套餐](https://bit.ly/BanWaGon)
