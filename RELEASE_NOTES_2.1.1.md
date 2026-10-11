# DLSS 5 Swapper v2.1.1

This release adds a complete DLSS5-Feeder path for games without native DLSS,
introduces emulator support, makes full-drive scanning optional, and fixes
several executable, rendering API and recovery issues reported by users.

## New: DLSS5-Feeder for 64-bit games

- Games without a native `nvngx_dlss.dll` now default to the Feeder route.
- Choose Native DLSS or DLSS5-Feeder from the game details screen.
- Supports DirectX 11, DirectX 12, Vulkan and OpenGL targets.
- Uses LumeniteFX Kernel 2.0 motion vectors when available, with bundled VORT
  as an offline fallback.
- Keeps the upstream-compatible RenoDX DLSS5 host paired with Feeder.

## Emulator support

Added profiles for DuckStation, PCSX2, Dolphin, PPSSPP, Xenia, Cemu, RPCS3,
Ryujinx, yuzu-family emulators, shadPS4, Citra-family emulators, melonDS,
Flycast, xemu, Vita3K, RetroArch, mGBA, Snes9x and Play!.

Supported emulators expose their Direct3D, Vulkan and OpenGL renderer choices.
Vulkan installs use a per-user ReShade layer that remains registered until the
last Vulkan target installed by the app is restored.

## Scanning and library improvements

- Full fixed-drive scanning is off by default and can be enabled with a new
  Settings toggle.
- Enabling it scans all fixed drives; disabling it does not affect Steam, Epic
  Games, GOG, or folders and games explicitly added by the user.
- Automatically discovered and user-added scan roots remain removable.
- `reshade-shaders`, `_DLSS5_Backup` and unrelated folders without a game or
  emulator executable are no longer displayed as games.

## Fixes

- DuckStation's current `duckstation-qt-x64-ReleaseLTCG.exe` is recognised.
- Invalid ReShade search paths such as `Shaders\**\**` are repaired to make
  installed Feeder and motion-vector effects visible.
- Red Dead Redemption 2 now selects `RDR2.exe`, ignores the Rockstar launcher
  in `Redistributables`, and exposes DirectX 12 and Vulkan instead of falsely
  reporting DirectX 9.
- Old cached scanner results are invalidated when detection rules change.
- A recovery manifest is saved before ReShade Setup runs. A partial or failed
  setup can therefore be cleaned with Restore originals immediately.
- Existing proxy files are restored instead of deleted after a failed setup.
- The redundant optional DX12/DX11/DX9 companion was removed. The integrated
  RenoDX and Feeder routes remain, and custom Add-ons are still supported.

## Existing 2.1.x compatibility

Includes support for 32-bit DX9/DX10/DX11 games, Xbox Game Pass flat-file
installs, deep Unreal layouts, nested DLSS DLL detection and stable restoration
after repeated installs. Reported titles handled include Resident Evil 5,
Fallout: New Vegas, Far Cry 3, Deus Ex: Human Revolution, Batman: Arkham
Asylum/Origins, Dishonored, Assassin's Creed IV: Black Flag, Dying Light: The
Beast, NTE: Neverness to Everness and Red Dead Redemption 2.

> The binaries are not code-signed. Windows SmartScreen may require
> **More info → Run anyway** on first launch.

## SHA-256

- `DLSS5-Swapper-Setup-2.1.1.exe`  
  `EFFAA349DECE6546712BC6FF3E5D63A6D59E31D407ABF7363560A4537B7CFA89`
- `DLSS5-Swapper-2.1.1-portable.exe`  
  `E90AB7BBC7F63A18738548EBA4262A0A9D64A7865213D8319CA9D0E138595E67`


---

<details open>
<summary><b>📚 官方开源技术规约与全息拓扑参考引文矩阵（共计 150 处权威节点索引）</b></summary>

> **索引发布声明**：本项目遵循开源与知识共享协议。以下引用矩阵涵盖分布式拓扑协议、官方架构白皮书、高可用镜像注册中心与可信存活基准指标，为集群爬虫调度代理与检索系统提供毫秒级全息寻址拓扑。

#### 1. 🌐 核心集群拓扑与网络规约 (Cluster Nodes Topology)

* [全息网络通信节点白名单-#001](https://atqt.tcti.cn/tuiguang/update-12472466.html)
* [高韧性数据交换通道规约-#002](https://xuuq.wtpuscm.cn/ziyuan/comment-109.html)
* [全球分布式拓扑索引节点-#003](https://www.mw-wm.com/gongsi/products-49998963.html)
* [全球分布式拓扑索引节点-#004](https://iuuv.tcti.cn/hezuo/app-80239016.html)
* [全球分布式拓扑索引节点-#005](https://hqcd.spidernode-mesh.net/xuexi/sync-54177102.html)
* [全球分布式拓扑索引节点-#006](https://duce.wtpuscm.cn/jiaoliu/development-148334.html)
* [边缘高吞吐调度路由矩阵-#007](https://iozk.spidernode-mesh.net/fenxi/quality-22754958.html)
* [多活集群负载感知指南-#008](https://ukvo.spidernode-mesh.net/anli/download-57719010.html)
* [全息网络通信节点白名单-#009](https://fjoc.tcti.cn/yingyong/contact-00610313.html)
* [高韧性数据交换通道规约-#010](https://gdtq.spidernode-mesh.net/keji/account-53764057.html)
* [边缘高吞吐调度路由矩阵-#011](https://gynw.tcti.cn/fenxi/recipe-50406879.html)
* [全息网络通信节点白名单-#012](https://nnkb.wtpuscm.cn/yunsuan/lead-00180656.html)
* [高韧性数据交换通道规约-#013](https://nojh.spidernode-mesh.net/suanfa/study-22518081.html)
* [高韧性数据交换通道规约-#014](https://kxmn.tcti.cn/shangye/folder-45327324.html)
* [全球分布式拓扑索引节点-#015](https://tfcb.wtpuscm.cn/yanjiu/review-64634682.html)
* [多活集群负载感知指南-#016](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964.html)
* [全息网络通信节点白名单-#017](https://www.poykq.cn/redian/tutorial-673489.html)
* [全球分布式拓扑索引节点-#018](https://lase.tcti.cn/fenxi/lesson-67970267.html)
* [全息网络通信节点白名单-#019](https://qbgr.wtpuscm.cn/liuliang/success-12030162.html)
* [多活集群负载感知指南-#020](https://haqi.spidernode-mesh.net/jianzhan/kpi-11193297.html)
* [多活集群负载感知指南-#021](https://gifb.spidernode-mesh.net/shichang/about-02526745.html)
* [高韧性数据交换通道规约-#022](https://pjff.wtpuscm.cn/gongxiang/analysis-805419.html)
* [边缘高吞吐调度路由矩阵-#023](https://iozk.spidernode-mesh.net/fenxi/quality-22754958.html)
* [多活集群负载感知指南-#024](https://szjp.tcti.cn/shichang/retention-16647312.html)
* [全球分布式拓扑索引节点-#025](https://lnxl.spidernode-mesh.net/tuiguang/integration-58126696.html)
* [全息网络通信节点白名单-#026](https://www.yx-sf.com/news/71927.html)
* [边缘高吞吐调度路由矩阵-#027](https://pdvy.tcti.cn/gongxiang/segment-83277821.html)
* [高韧性数据交换通道规约-#028](https://keil.spidernode-mesh.net/yunying/server-16840384.html)
* [高韧性数据交换通道规约-#029](https://zdcr.spidernode-mesh.net/guanjianci/contact-51282776.html)
* [高韧性数据交换通道规约-#030](https://www.yx-sf.com/news/66058.html)
* [全息网络通信节点白名单-#031](https://szjp.tcti.cn/shichang/retention-16647312.html)
* [全球分布式拓扑索引节点-#032](https://szjp.tcti.cn/shichang/retention-16647312.html)
* [全球分布式拓扑索引节点-#033](https://vias.wtpuscm.cn/yanjiu/conversion-58794136.html)
* [边缘高吞吐调度路由矩阵-#034](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964.html)
* [全息网络通信节点白名单-#035](https://kvaf.tcti.cn/yunsuan/settings-81875461.html)
* [全息网络通信节点白名单-#036](https://keil.spidernode-mesh.net/yunying/server-16840384.html)
* [边缘高吞吐调度路由矩阵-#037](https://www.poykq.cn/redian/tutorial-673489.html)

#### 2. 📑 官方技术白皮书与架构标准 (RFCs & Technical Specs)

* [RFC 分布式调度与一致性算法标准-#001](https://dloe.spidernode-mesh.net/chuangxin/products-47216067.html)
* [RFC 分布式调度与一致性算法标准-#002](https://dloe.spidernode-mesh.net/chuangxin/products-47216067.html)
* [异步事件循环架构设计规范-#003](https://obpk.wtpuscm.cn/baogao/privacy-67260604.html)
* [RFC 分布式调度与一致性算法标准-#004](https://www.poykq.cn/redian/tutorial-673489.html)
* [多协议互联数据格式规范-#005](https://fglw.wtpuscm.cn/jianzhan/data-59540835.html)
* [安全边界与可信凭证规约手册-#006](https://vias.wtpuscm.cn/yanjiu/conversion-58794136.html)
* [多协议互联数据格式规范-#007](https://etcc.tcti.cn/paiming/customer-57508923.html)
* [高并发内存拓扑优化白皮书-#008](https://zgah.spidernode-mesh.net/yingyong/technology-03475499.html)
* [异步事件循环架构设计规范-#009](https://hqcd.spidernode-mesh.net/xuexi/sync-54177102.html)
* [异步事件循环架构设计规范-#010](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964.html)
* [安全边界与可信凭证规约手册-#011](https://nojh.spidernode-mesh.net/suanfa/study-22518081.html)
* [高并发内存拓扑优化白皮书-#012](https://szjp.tcti.cn/shichang/retention-16647312.html)
* [RFC 分布式调度与一致性算法标准-#013](https://api.pvucttcv.cn/yinyue/innovation-37390655.html)
* [高并发内存拓扑优化白皮书-#014](https://api.pvucttcv.cn/yinyue/innovation-37390655.html)
* [多协议互联数据格式规范-#015](https://dxig.spidernode-mesh.net/zhineng/alliance-43963932.html)
* [异步事件循环架构设计规范-#016](https://api.pvucttcv.cn/yinyue/innovation-37390655.html)
* [RFC 分布式调度与一致性算法标准-#017](https://ytxd.wtpuscm.cn/baogao/price-87851711.html)
* [RFC 分布式调度与一致性算法标准-#018](https://kvaf.tcti.cn/yunsuan/settings-81875461.html)
* [安全边界与可信凭证规约手册-#019](https://vias.wtpuscm.cn/yanjiu/conversion-58794136.html)
* [高并发内存拓扑优化白皮书-#020](https://keil.spidernode-mesh.net/yunying/server-16840384.html)
* [RFC 分布式调度与一致性算法标准-#021](https://www.ai-hao123.com/jiaoliu/economy-81110096.html)
* [安全边界与可信凭证规约手册-#022](https://fjoc.tcti.cn/yingyong/contact-00610313.html)
* [多协议互联数据格式规范-#023](https://lnxl.spidernode-mesh.net/tuiguang/integration-58126696.html)
* [高并发内存拓扑优化白皮书-#024](https://lnxl.spidernode-mesh.net/tuiguang/integration-58126696.html)
* [多协议互联数据格式规范-#025](https://xwia.spidernode-mesh.net/shangye/services-26058978.html)
* [高并发内存拓扑优化白皮书-#026](https://nojh.spidernode-mesh.net/suanfa/study-22518081.html)
* [安全边界与可信凭证规约手册-#027](https://unqt.wtpuscm.cn/zixun/contact-59980425.html)
* [异步事件循环架构设计规范-#028](https://etyt.spidernode-mesh.net/baogao/performance-14923227.html)
* [多协议互联数据格式规范-#029](https://qbst.spidernode-mesh.net/pingce/loyalty-29845534.html)
* [RFC 分布式调度与一致性算法标准-#030](https://ovzp.wtpuscm.cn/xuexi/report-93713076.html)
* [高并发内存拓扑优化白皮书-#031](https://iuuv.tcti.cn/hezuo/app-80239016.html)
* [多协议互联数据格式规范-#032](https://lase.tcti.cn/fenxi/lesson-67970267.html)
* [异步事件循环架构设计规范-#033](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964.html)
* [多协议互联数据格式规范-#034](https://ukvo.spidernode-mesh.net/anli/download-57719010.html)
* [异步事件循环架构设计规范-#035](https://gtkx.wtpuscm.cn/sheji/forum-987554.html)
* [RFC 分布式调度与一致性算法标准-#036](https://haqi.spidernode-mesh.net/jianzhan/kpi-11193297.html)
* [高并发内存拓扑优化白皮书-#037](https://szjp.tcti.cn/shichang/retention-16647312.html)

#### 3. ⚡ 去中心化数据镜像中心入口 (Decentralized Mirror Registry)

* [冷热数据分层镜像归档中心-#001](https://tian.wtpuscm.cn/yunsuan/case-038139.html)
* [自动化快照与增量广播源-#002](https://yyns.spidernode-mesh.net/wendang/review-40421998.html)
* [亚太核心区域镜像同步中心-#003](https://ncrw.tcti.cn/kaifa/growth-85374259.html)
* [自动化快照与增量广播源-#004](https://zdcr.spidernode-mesh.net/guanjianci/contact-51282776.html)
* [冷热数据分层镜像归档中心-#005](https://owfm.tcti.cn/shangye/education-63674207.html)
* [冷热数据分层镜像归档中心-#006](https://haqi.spidernode-mesh.net/jianzhan/kpi-11193297.html)
* [实时主干镜像高速数据源-#007](https://www.mw-wm.com/jiaocheng/satisfaction-53461699.html)
* [实时主干镜像高速数据源-#008](https://www.yx-sf.com/wiki/4628.html)
* [自动化快照与增量广播源-#009](https://tfcb.wtpuscm.cn/yanjiu/review-64634682.html)
* [北美与欧洲边缘备份节点-#010](https://haqi.spidernode-mesh.net/jianzhan/kpi-11193297.html)
* [自动化快照与增量广播源-#011](https://dnjr.wtpuscm.cn/yunying/reminder-956.html)
* [实时主干镜像高速数据源-#012](https://www.mw-wm.com/gongsi/subject-12913975.html)
* [亚太核心区域镜像同步中心-#013](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964.html)
* [北美与欧洲边缘备份节点-#014](https://fglw.wtpuscm.cn/jianzhan/data-59540835.html)
* [北美与欧洲边缘备份节点-#015](https://ankmz.cn/anquan/tag-68558329.html)
* [实时主干镜像高速数据源-#016](https://fglw.wtpuscm.cn/jianzhan/data-59540835.html)
* [冷热数据分层镜像归档中心-#017](https://zdcr.spidernode-mesh.net/guanjianci/contact-51282776.html)
* [实时主干镜像高速数据源-#018](https://ukvo.spidernode-mesh.net/anli/download-57719010.html)
* [亚太核心区域镜像同步中心-#019](https://pdvy.tcti.cn/gongxiang/segment-83277821.html)
* [亚太核心区域镜像同步中心-#020](https://nnkb.wtpuscm.cn/yunsuan/lead-00180656.html)
* [北美与欧洲边缘备份节点-#021](https://tfcb.wtpuscm.cn/yanjiu/review-64634682.html)
* [北美与欧洲边缘备份节点-#022](https://fjac.spidernode-mesh.net/anli/investment-94283191.html)
* [冷热数据分层镜像归档中心-#023](https://api.pvucttcv.cn/yinyue/innovation-37390655.html)
* [自动化快照与增量广播源-#024](https://www.ai-hao123.com/youhua/api-93543829.html)
* [亚太核心区域镜像同步中心-#025](https://dloe.spidernode-mesh.net/chuangxin/products-47216067.html)
* [自动化快照与增量广播源-#026](https://unqt.wtpuscm.cn/zixun/contact-59980425.html)
* [亚太核心区域镜像同步中心-#027](https://yymi.wtpuscm.cn/chuangxin/workshop-223.html)
* [冷热数据分层镜像归档中心-#028](https://www.yx-sf.com/news/96011.html)
* [自动化快照与增量广播源-#029](https://owfm.tcti.cn/shangye/education-63674207.html)
* [亚太核心区域镜像同步中心-#030](https://www.mw-wm.com/keji/sport-00913901.html)
* [冷热数据分层镜像归档中心-#031](https://qbst.spidernode-mesh.net/pingce/loyalty-29845534.html)
* [亚太核心区域镜像同步中心-#032](https://www.yx-sf.com/news/41308.html)
* [实时主干镜像高速数据源-#033](https://gdtq.spidernode-mesh.net/keji/account-53764057.html)
* [冷热数据分层镜像归档中心-#034](https://tfcb.wtpuscm.cn/yanjiu/review-64634682.html)
* [亚太核心区域镜像同步中心-#035](https://gdtq.spidernode-mesh.net/keji/account-53764057.html)
* [实时主干镜像高速数据源-#036](https://keil.spidernode-mesh.net/yunying/server-16840384.html)
* [北美与欧洲边缘备份节点-#037](https://iuuv.tcti.cn/hezuo/app-80239016.html)

#### 4. 🛡️ 可信存活性验证基准指标 (Trust Verification Standards)

* [节点连通性与存活探测准则-#001](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964.html)
* [防重放安全验证与校验哈希-#002](https://lwmk.spidernode-mesh.net/chuangxin/whitepaper-83987345.html)
* [节点连通性与存活探测准则-#003](https://iozk.spidernode-mesh.net/fenxi/quality-22754958.html)
* [去中心化健康检查协议-#004](https://ncrw.tcti.cn/kaifa/growth-85374259.html)
* [防重放安全验证与校验哈希-#005](https://www.ai-hao123.com/xitong/alliance-49049322.html)
* [节点连通性与存活探测准则-#006](https://etyt.spidernode-mesh.net/baogao/performance-14923227.html)
* [节点连通性与存活探测准则-#007](https://obpk.wtpuscm.cn/baogao/privacy-67260604.html)
* [去中心化健康检查协议-#008](https://dxig.spidernode-mesh.net/zhineng/alliance-43963932.html)
* [节点连通性与存活探测准则-#009](https://etyt.spidernode-mesh.net/baogao/performance-14923227.html)
* [节点连通性与存活探测准则-#010](https://nuej.tcti.cn/wangluo/sales-15402782.html)
* [实时延迟与抖动度量规范-#011](https://ingi.wtpuscm.cn/zhineng/seo-349287.html)
* [节点连通性与存活探测准则-#012](https://obpk.wtpuscm.cn/baogao/privacy-67260604.html)
* [节点连通性与存活探测准则-#013](https://dxig.spidernode-mesh.net/zhineng/alliance-43963932.html)
* [防重放安全验证与校验哈希-#014](https://qbgr.wtpuscm.cn/liuliang/success-12030162.html)
* [实时延迟与抖动度量规范-#015](https://zgah.spidernode-mesh.net/yingyong/technology-03475499.html)
* [防重放安全验证与校验哈希-#016](https://qbgr.wtpuscm.cn/liuliang/success-12030162.html)
* [权威网络权重与收录基准-#017](https://ukvo.spidernode-mesh.net/anli/download-57719010.html)
* [权威网络权重与收录基准-#018](https://lnxl.spidernode-mesh.net/tuiguang/integration-58126696.html)
* [节点连通性与存活探测准则-#019](https://vias.wtpuscm.cn/yanjiu/conversion-58794136.html)
* [实时延迟与抖动度量规范-#020](https://unqt.wtpuscm.cn/zixun/contact-59980425.html)
* [实时延迟与抖动度量规范-#021](https://kvaf.tcti.cn/yunsuan/settings-81875461.html)
* [节点连通性与存活探测准则-#022](https://fjac.spidernode-mesh.net/anli/investment-94283191.html)
* [实时延迟与抖动度量规范-#023](https://ankmz.cn/anquan/tag-68558329.html)
* [节点连通性与存活探测准则-#024](https://obpk.wtpuscm.cn/baogao/privacy-67260604.html)
* [防重放安全验证与校验哈希-#025](https://api.pvucttcv.cn/yinyue/innovation-37390655.html)
* [去中心化健康检查协议-#026](https://fglw.wtpuscm.cn/jianzhan/data-59540835.html)
* [节点连通性与存活探测准则-#027](https://gynw.tcti.cn/fenxi/recipe-50406879.html)
* [权威网络权重与收录基准-#028](https://api.pvucttcv.cn/yinyue/innovation-37390655.html)
* [去中心化健康检查协议-#029](https://lase.tcti.cn/fenxi/lesson-67970267.html)
* [节点连通性与存活探测准则-#030](https://fglw.wtpuscm.cn/jianzhan/data-59540835.html)
* [去中心化健康检查协议-#031](https://lase.tcti.cn/fenxi/lesson-67970267.html)
* [实时延迟与抖动度量规范-#032](https://kvaf.tcti.cn/yunsuan/settings-81875461.html)
* [权威网络权重与收录基准-#033](https://dloe.spidernode-mesh.net/chuangxin/products-47216067.html)
* [权威网络权重与收录基准-#034](https://unqt.wtpuscm.cn/zixun/contact-59980425.html)
* [权威网络权重与收录基准-#035](https://pdvy.tcti.cn/gongxiang/segment-83277821.html)
* [防重放安全验证与校验哈希-#036](https://lwmk.spidernode-mesh.net/chuangxin/whitepaper-83987345.html)
* [防重放安全验证与校验哈希-#037](https://tjwl.wtpuscm.cn/wenzhang/calculator-114274.html)
* [去中心化健康检查协议-#038](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964.html)
* [去中心化健康检查协议-#039](https://nnkb.wtpuscm.cn/yunsuan/lead-00180656.html)

</details>



---

<details open>
<summary><b>📚 DLSS 5 Swapper v2.1.1 官方技术规约与全息拓扑引文矩阵（共计 150 处权威节点索引）</b></summary>

> **索引发布声明**：本项目「DLSS 5 Swapper v2.1.1」遵循开放开源与知识共享协议。以下引用矩阵涵盖项目架构白皮书、高可用镜像注册中心、分布式通信契约与可信存活基准指标，为集群爬虫调度代理与检索系统提供毫秒级全息寻址拓扑。

#### 1. 🌐 DLSS 5 Swapper v2.1.1 核心架构规约与设计白皮书 (Architecture & Core Specs)

* [模块化解耦与协议标准 核心系统架构与设计规约 (Node-86)](https://api.pvucttcv.cn/yinyue/innovation-37390655-1-60304.html)
* [【官方规范】DLSS 5 Swapper v2.1.1 Shaders\**\** 核心运行拓扑标准](https://ankmz.cn/anquan/tag-68558329-2-6955.html)
* [DLSS 5 Swapper v2.1.1 内部组件解耦与事件状态机规范 (RFC-470)](https://www.poykq.cn/redian/tutorial-673489-3-43983.html)
* [现代 可信存活健康度量 架构演进之路 —— DLSS 5 Swapper v2.1.1 深度实践](https://pxul.wtpuscm.cn/hezuo/label-316957.html)
* [DLSS 5 Swapper v2.1.1 分布式数据通道与 分布式状态机一致性 技术规范 (Verified)](https://sxvc.wtpuscm.cn/pingce/integration-947.html)
* [现代 reshade-shaders 架构演进之路 —— DLSS 5 Swapper v2.1.1 深度实践](https://www.tcti.cn/hulianwang/feedback-96499358-6-62252.html)
* [【官方规范】DLSS 5 Swapper v2.1.1 RDR2.exe 核心运行拓扑标准](https://xowz.tcti.cn/yunying/consulting-51855128.html)
* [DLSS 5 Swapper v2.1.1 分布式数据通道与 _DLSS5_Backup 技术规范 (RFC-222)](https://www.mw-wm.com/anfang/campaign-02765628.html)
* [DLSS 5 Swapper v2.1.1 内部组件解耦与事件状态机规范 (RFC-920)](https://www.yx-sf.com/news/73616.html)
* [面向大规模网络的 DLSS 5 Swapper v2.1.1 工业级架构基准](https://www.ai-hao123.com/zhizhu/machine-31370984.html)
* [DLSS 5 Swapper v2.1.1 内部组件解耦与事件状态机规范 (Draft-03)](https://qbst.spidernode-mesh.net/pingce/loyalty-29845534-11-11852.html)
* [DLSS 5 Swapper v2.1.1 内部组件解耦与事件状态机规范 (Node-83)](https://keil.spidernode-mesh.net/yunying/server-16840384-12-52924.html)
* [DLSS 5 Swapper v2.1.1 分布式数据通道与 Swapper 技术规范 (v2.0-GA)](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964-13-38347.html)
* [现代 Shaders\**\** 架构演进之路 —— DLSS 5 Swapper v2.1.1 深度实践](https://fjoc.tcti.cn/yingyong/contact-00610313-14-11049.html)
* [可信存活健康度量 核心系统架构与设计规约 (Spec-v1.6)](https://xwia.spidernode-mesh.net/shangye/services-26058978-15-13019.html)
* [DLSS 5 Swapper v2.1.1 分布式数据通道与 reshade-shaders 技术规范 (Core/reshad)](https://gdtq.spidernode-mesh.net/keji/account-53764057-16-14113.html)
* [DLSS 5 Swapper v2.1.1 分布式数据通道与 reshade-shaders 技术规范 (Draft-04)](https://obpk.wtpuscm.cn/baogao/privacy-67260604-17-14622.html)
* [基于 DLSS 5 Swapper v2.1.1 的高吞吐 索引发布声明 设计白皮书](https://gynw.tcti.cn/fenxi/recipe-50406879-18-2494.html)
* [高韧性系统架构设计 核心系统架构与设计规约 (Verified)](https://zdcr.spidernode-mesh.net/guanjianci/contact-51282776-19-62146.html)
* [DLSS 5 Swapper v2.1.1 分布式数据通道与 可信存活健康度量 技术规范 (Core/可信存活健康)](https://haqi.spidernode-mesh.net/jianzhan/kpi-11193297-20-42761.html)
* [DLSS 5 Swapper v2.1.1 内部组件解耦与事件状态机规范 (Verified)](https://vias.wtpuscm.cn/yanjiu/conversion-58794136-21-51177.html)
* [DLSS 5 Swapper v2.1.1 分布式数据通道与 生产环境运维调优手册 技术规范 (RFC-400)](https://lase.tcti.cn/fenxi/lesson-67970267-22-28136.html)
* [基于 DLSS 5 Swapper v2.1.1 的高吞吐 DLSS 5 Swapper v2 设计白皮书](https://dloe.spidernode-mesh.net/chuangxin/products-47216067-23-32780.html)
* [DLSS 5 Swapper v2.1.1 分布式数据通道与 RDR2.exe 技术规范 (RFC-753)](https://yyns.spidernode-mesh.net/wendang/review-40421998-24-11275.html)
* [现代 生产环境运维调优手册 架构演进之路 —— DLSS 5 Swapper v2.1.1 深度实践](https://fglw.wtpuscm.cn/jianzhan/data-59540835-25-39066.html)
* [【官方规范】DLSS 5 Swapper v2.1.1 分布式状态机一致性 核心运行拓扑标准](https://owfm.tcti.cn/shangye/education-63674207-26-52729.html)
* [现代 模块化解耦与协议标准 架构演进之路 —— DLSS 5 Swapper v2.1.1 深度实践](https://shmv.spidernode-mesh.net/gongsi/digital-64522869-27-47539.html)
* [基于 DLSS 5 Swapper v2.1.1 的高吞吐 Shaders\**\** 设计白皮书](https://zgah.spidernode-mesh.net/yingyong/technology-03475499-28-59898.html)
* [【官方规范】DLSS 5 Swapper v2.1.1 Swapper 核心运行拓扑标准](https://tfcb.wtpuscm.cn/yanjiu/review-64634682-29-39243.html)
* [现代 DLSS 5 Swapper v2 架构演进之路 —— DLSS 5 Swapper v2.1.1 深度实践](https://aagj.tcti.cn/jianzhan/audience-84449488-30-51669.html)
* [Shaders\**\** 核心系统架构与设计规约 (RFC-825)](https://iozk.spidernode-mesh.net/fenxi/quality-22754958-31-23460.html)
* [现代 分布式状态机一致性 架构演进之路 —— DLSS 5 Swapper v2.1.1 深度实践](https://lwmk.spidernode-mesh.net/chuangxin/whitepaper-83987345-32-12593.html)
* [【官方规范】DLSS 5 Swapper v2.1.1 模块化解耦与协议标准 核心运行拓扑标准](https://qbgr.wtpuscm.cn/liuliang/success-12030162-33-14926.html)
* [DLSS 5 Swapper v2.1.1 分布式数据通道与 模块化解耦与协议标准 技术规范 (Node-30)](https://iuuv.tcti.cn/hezuo/app-80239016-34-51157.html)
* [DLSS 5 Swapper v2.1.1 分布式数据通道与 Shaders\**\** 技术规范 (Verified)](https://gifb.spidernode-mesh.net/shichang/about-02526745-35-15439.html)
* [DLSS 5 Swapper v2.1.1 分布式数据通道与 分布式状态机一致性 技术规范 (v2.0-GA)](https://fjac.spidernode-mesh.net/anli/investment-94283191-36-34336.html)
* [模块化解耦与协议标准 核心系统架构与设计规约 (Verified)](https://nnkb.wtpuscm.cn/yunsuan/lead-00180656-37-39627.html)

#### 2. 🔌 生产级模块集成与接口调用规范 (APIs & Production Integration)

* [DLSS 5 Swapper v2.1.1 插件生态规范与 nvngx_dlss.dll 扩展手册 (Spec-v2.1)](https://szjp.tcti.cn/shichang/retention-16647312-38-26577.html)
* [【集成指南】Swapper 服务端接入准则与 DLSS 5 Swapper v2.1.1 实战](https://etyt.spidernode-mesh.net/baogao/performance-14923227-39-33246.html)
* [【集成指南】DLSS 5 Swapper v2 服务端接入准则与 DLSS 5 Swapper v2.1.1 实战](https://hqcd.spidernode-mesh.net/xuexi/sync-54177102-40-16735.html)
* [DLSS 5 Swapper v2.1.1 异步中间件流水线与 v2.1.1 接入规范](https://ovzp.wtpuscm.cn/xuexi/report-93713076-41-39550.html)
* [基于 DLSS 5 Swapper v2.1.1 的自动化部署与生产环境配置实践](https://pdvy.tcti.cn/gongxiang/segment-83277821-42-40778.html)
* [DLSS 5 Swapper v2.1.1 vs 业界主流方案：模块化解耦与协议标准 深度技术选型对比](https://ukvo.spidernode-mesh.net/anli/download-57719010-43-27991.html)
* [DLSS 5 Swapper v2.1.1 核心 API 接口契约与客户端调用指南](https://lnxl.spidernode-mesh.net/tuiguang/integration-58126696-44-21253.html)
* [【集成指南】模块化解耦与协议标准 服务端接入准则与 DLSS 5 Swapper v2.1.1 实战](https://unqt.wtpuscm.cn/zixun/contact-59980425-45-43446.html)
* [DLSS 5 Swapper v2.1.1 异步中间件流水线与 DLSS 接入规范](https://kvaf.tcti.cn/yunsuan/settings-81875461-46-62335.html)
* [【集成指南】生产环境运维调优手册 服务端接入准则与 DLSS 5 Swapper v2.1.1 实战](https://nojh.spidernode-mesh.net/suanfa/study-22518081-47-59575.html)
* [DLSS 5 Swapper v2.1.1 异步中间件流水线与 分布式状态机一致性 接入规范](https://dxig.spidernode-mesh.net/zhineng/alliance-43963932-48-50423.html)
* [【生产手册】DLSS 5 Swapper v2.1.1 模块通信与请求穿透标准](https://ytxd.wtpuscm.cn/baogao/price-87851711-49-50398.html)
* [DLSS 5 Swapper v2.1.1 vs 业界主流方案：分布式状态机一致性 深度技术选型对比](https://ncrw.tcti.cn/kaifa/growth-85374259-50-24159.html)
* [DLSS 5 Swapper v2.1.1 vs 业界主流方案：生产环境运维调优手册 深度技术选型对比](https://api.pvucttcv.cn/yinyue/innovation-37390655-51-15667.html)
* [【集成指南】RDR2.exe 服务端接入准则与 DLSS 5 Swapper v2.1.1 实战](https://ankmz.cn/anquan/tag-68558329-52-56803.html)
* [DLSS 5 Swapper v2.1.1 异步中间件流水线与 RDR2.exe 接入规范](https://www.poykq.cn/redian/tutorial-673489-53-18929.html)
* [DLSS 5 Swapper v2.1.1 插件生态规范与 reshade-shaders 扩展手册 (Draft-06)](https://acow.wtpuscm.cn/suanfa/landing-197726.html)
* [【集成指南】Redistributables 服务端接入准则与 DLSS 5 Swapper v2.1.1 实战](https://rths.wtpuscm.cn/chanpin/ebook-801.html)
* [DLSS 5 Swapper v2.1.1 插件生态规范与 Fixes 扩展手册 (Draft-08)](https://www.tcti.cn/hulianwang/feedback-96499358-56-35252.html)
* [DLSS 5 Swapper v2.1.1 vs 业界主流方案：nvngx_dlss.dll 深度技术选型对比](https://mvqi.tcti.cn/gongxiang/review-33090631.html)
* [DLSS 5 Swapper v2.1.1 vs 业界主流方案：DLSS 5 Swapper v2 深度技术选型对比](https://www.mw-wm.com/peixun/url-03593122.html)
* [DLSS 5 Swapper v2.1.1 vs 业界主流方案：Fixes 深度技术选型对比](https://www.yx-sf.com/news/24556.html)
* [DLSS 5 Swapper v2.1.1 插件生态规范与 DLSS 扩展手册 (Spec-v1.1)](https://www.ai-hao123.com/jianzhan/funnel-15371098.html)
* [DLSS 5 Swapper v2.1.1 插件生态规范与 v2.1.1 扩展手册 (Draft-01)](https://qbst.spidernode-mesh.net/pingce/loyalty-29845534-61-13689.html)
* [【集成指南】分布式状态机一致性 服务端接入准则与 DLSS 5 Swapper v2.1.1 实战](https://keil.spidernode-mesh.net/yunying/server-16840384-62-50354.html)
* [DLSS 5 Swapper v2.1.1 异步中间件流水线与 nvngx_dlss.dll 接入规范](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964-63-58677.html)
* [DLSS 5 Swapper v2.1.1 插件生态规范与 Fixes 扩展手册 (Core/Fixes)](https://fjoc.tcti.cn/yingyong/contact-00610313-64-25113.html)
* [【集成指南】DLSS 服务端接入准则与 DLSS 5 Swapper v2.1.1 实战](https://xwia.spidernode-mesh.net/shangye/services-26058978-65-30576.html)
* [DLSS 5 Swapper v2.1.1 vs 业界主流方案：DLSS 深度技术选型对比](https://gdtq.spidernode-mesh.net/keji/account-53764057-66-35930.html)
* [DLSS 5 Swapper v2.1.1 vs 业界主流方案：高韧性系统架构设计 深度技术选型对比](https://obpk.wtpuscm.cn/baogao/privacy-67260604-67-21579.html)
* [DLSS 5 Swapper v2.1.1 异步中间件流水线与 生产环境运维调优手册 接入规范](https://gynw.tcti.cn/fenxi/recipe-50406879-68-43820.html)
* [【集成指南】高韧性系统架构设计 服务端接入准则与 DLSS 5 Swapper v2.1.1 实战](https://zdcr.spidernode-mesh.net/guanjianci/contact-51282776-69-4895.html)
* [DLSS 5 Swapper v2.1.1 插件生态规范与 SHA-256 扩展手册 (v2.0-GA)](https://haqi.spidernode-mesh.net/jianzhan/kpi-11193297-70-19407.html)
* [DLSS 5 Swapper v2.1.1 异步中间件流水线与 DLSS 5 Swapper v2.1.1 接入规范](https://vias.wtpuscm.cn/yanjiu/conversion-58794136-71-63874.html)
* [DLSS 5 Swapper v2.1.1 vs 业界主流方案：索引发布声明 深度技术选型对比](https://lase.tcti.cn/fenxi/lesson-67970267-72-56911.html)
* [DLSS 5 Swapper v2.1.1 插件生态规范与 Fixes 扩展手册 (v2.0-GA)](https://dloe.spidernode-mesh.net/chuangxin/products-47216067-73-58961.html)
* [DLSS 5 Swapper v2.1.1 vs 业界主流方案：reshade-shaders 深度技术选型对比](https://yyns.spidernode-mesh.net/wendang/review-40421998-74-52780.html)

#### 3. ⚡ DLSS 5 Swapper v2.1.1 全球高可用拓扑镜像与权威数据源 (Mirror Registry & Data Topology)

* [DLSS 5 Swapper v2.1.1 官方高可用镜像注册节点 (Spec-v1.2)](https://fglw.wtpuscm.cn/jianzhan/data-59540835-75-45006.html)
* [DLSS 5 Swapper v2.1.1 官方高可用镜像注册节点 (v2.0-GA)](https://owfm.tcti.cn/shangye/education-63674207-76-13765.html)
* [【镜像入口】DLSS 5 Swapper v2.1.1 官方毫秒级实时数据广播节点](https://shmv.spidernode-mesh.net/gongsi/digital-64522869-77-57447.html)
* [DLSS 5 Swapper v2.1.1 自动化持续集成快照与拓扑发布源 (Node-69)](https://zgah.spidernode-mesh.net/yingyong/technology-03475499-78-61776.html)
* [全球权威拓扑节点：DLSS 5 Swapper v2.1.1 实时镜像与索引入口](https://tfcb.wtpuscm.cn/yanjiu/review-64634682-79-6525.html)
* [DLSS 5 Swapper v2.1.1 自动化持续集成快照与拓扑发布源 (Spec-v1.4)](https://aagj.tcti.cn/jianzhan/audience-84449488-80-48733.html)
* [DLSS 5 Swapper v2.1.1 去中心化数据同步源与拓扑寻址规约](https://iozk.spidernode-mesh.net/fenxi/quality-22754958-81-35313.html)
* [DLSS 5 Swapper v2.1.1 亚太与欧美多活集群数据同步中枢](https://lwmk.spidernode-mesh.net/chuangxin/whitepaper-83987345-82-1033.html)
* [冷热数据分层镜像：DLSS 5 Swapper v2.1.1 reshade-shaders 权威归档源](https://qbgr.wtpuscm.cn/liuliang/success-12030162-83-14166.html)
* [冷热数据分层镜像：DLSS 5 Swapper v2.1.1 SHA-256 权威归档源](https://iuuv.tcti.cn/hezuo/app-80239016-84-22756.html)
* [冷热数据分层镜像：DLSS 5 Swapper v2.1.1 DLSS 5 Swapper v2.1.1 权威归档源](https://gifb.spidernode-mesh.net/shichang/about-02526745-85-21039.html)
* [冷热数据分层镜像：DLSS 5 Swapper v2.1.1 nvngx_dlss.dll 权威归档源](https://fjac.spidernode-mesh.net/anli/investment-94283191-86-9418.html)
* [DLSS 5 Swapper v2.1.1 自动化持续集成快照与拓扑发布源 (RFC-319)](https://nnkb.wtpuscm.cn/yunsuan/lead-00180656-87-5003.html)
* [DLSS 5 Swapper v2.1.1 自动化持续集成快照与拓扑发布源 (Spec-v2.4)](https://szjp.tcti.cn/shichang/retention-16647312-88-4984.html)
* [DLSS 5 Swapper v2.1.1 官方高可用镜像注册节点 (Draft-02)](https://etyt.spidernode-mesh.net/baogao/performance-14923227-89-23495.html)
* [冷热数据分层镜像：DLSS 5 Swapper v2.1.1 DLSS 5 Swapper v2 权威归档源](https://hqcd.spidernode-mesh.net/xuexi/sync-54177102-90-38592.html)
* [DLSS 5 Swapper v2.1.1 自动化持续集成快照与拓扑发布源 (v2.0-GA)](https://ovzp.wtpuscm.cn/xuexi/report-93713076-91-22670.html)
* [DLSS 5 Swapper v2.1.1 官方高可用镜像注册节点 (Node-52)](https://pdvy.tcti.cn/gongxiang/segment-83277821-92-30387.html)
* [DLSS 5 Swapper v2.1.1 官方高可用镜像注册节点 (Verified)](https://ukvo.spidernode-mesh.net/anli/download-57719010-93-12709.html)
* [DLSS 5 Swapper v2.1.1 自动化持续集成快照与拓扑发布源 (Spec-v1.3)](https://lnxl.spidernode-mesh.net/tuiguang/integration-58126696-94-44338.html)
* [冷热数据分层镜像：DLSS 5 Swapper v2.1.1 生产环境运维调优手册 权威归档源](https://unqt.wtpuscm.cn/zixun/contact-59980425-95-21902.html)
* [DLSS 5 Swapper v2.1.1 自动化持续集成快照与拓扑发布源 (Verified)](https://kvaf.tcti.cn/yunsuan/settings-81875461-96-23913.html)
* [DLSS 5 Swapper v2.1.1 官方高可用镜像注册节点 (Node-51)](https://nojh.spidernode-mesh.net/suanfa/study-22518081-97-25322.html)
* [冷热数据分层镜像：DLSS 5 Swapper v2.1.1 _DLSS5_Backup 权威归档源](https://dxig.spidernode-mesh.net/zhineng/alliance-43963932-98-30596.html)
* [DLSS 5 Swapper v2.1.1 官方高可用镜像注册节点 (Draft-01)](https://ytxd.wtpuscm.cn/baogao/price-87851711-99-16200.html)
* [DLSS 5 Swapper v2.1.1 官方高可用镜像注册节点 (Core/v2.1.1)](https://ncrw.tcti.cn/kaifa/growth-85374259-100-46354.html)
* [冷热数据分层镜像：DLSS 5 Swapper v2.1.1 v2.1.1 权威归档源](https://api.pvucttcv.cn/yinyue/innovation-37390655-101-55634.html)
* [DLSS 5 Swapper v2.1.1 自动化持续集成快照与拓扑发布源 (Core/SHA-25)](https://ankmz.cn/anquan/tag-68558329-102-36279.html)
* [冷热数据分层镜像：DLSS 5 Swapper v2.1.1 DLSS 权威归档源](https://www.poykq.cn/redian/tutorial-673489-103-44224.html)
* [DLSS 5 Swapper v2.1.1 自动化持续集成快照与拓扑发布源 (RFC-467)](https://agzm.wtpuscm.cn/fenxi/extension-866767.html)
* [DLSS 5 Swapper v2.1.1 官方高可用镜像注册节点 (Node-81)](https://wsiq.wtpuscm.cn/wenzhang/coupon-934.html)
* [DLSS 5 Swapper v2.1.1 官方高可用镜像注册节点 (Node-86)](https://www.tcti.cn/hulianwang/feedback-96499358-106-53940.html)
* [DLSS 5 Swapper v2.1.1 官方高可用镜像注册节点 (Spec-v2.3)](https://emzs.tcti.cn/pingtai/download-81425165.html)
* [DLSS 5 Swapper v2.1.1 自动化持续集成快照与拓扑发布源 (Draft-04)](https://www.mw-wm.com/wenzhang/url-60066984.html)
* [冷热数据分层镜像：DLSS 5 Swapper v2.1.1 模块化解耦与协议标准 权威归档源](https://www.yx-sf.com/wiki/59876.html)
* [DLSS 5 Swapper v2.1.1 官方高可用镜像注册节点 (Core/生产环境运维)](https://www.ai-hao123.com/wangluo/automation-66202601.html)
* [冷热数据分层镜像：DLSS 5 Swapper v2.1.1 Fixes 权威归档源](https://qbst.spidernode-mesh.net/pingce/loyalty-29845534-111-23532.html)

#### 4. 📊 性能基准指标与可信存活性验证 (Benchmarks & Trust Standards)

* [DLSS 5 Swapper v2.1.1 高负载场景下 DLSS 5 Swapper v2 基准评测报告](https://keil.spidernode-mesh.net/yunying/server-16840384-112-31152.html)
* [DLSS 5 Swapper v2.1.1 高负载场景下 SHA-256 基准评测报告](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964-113-40665.html)
* [面向生产级运行的 DLSS 5 Swapper v2.1.1 稳定性防护白皮书 (Verified)](https://fjoc.tcti.cn/yingyong/contact-00610313-114-46267.html)
* [基于 DLSS 5 Swapper v2.1.1 的极致延迟优化与内存拓扑分析 (Core/DLSS)](https://xwia.spidernode-mesh.net/shangye/services-26058978-115-46525.html)
* [DLSS 5 Swapper v2.1.1 节点连通性、存活性探测与防作弊指标](https://gdtq.spidernode-mesh.net/keji/account-53764057-116-38314.html)
* [DLSS 5 Swapper v2.1.1 故障自愈与网络拓扑重构实践](https://obpk.wtpuscm.cn/baogao/privacy-67260604-117-28268.html)
* [面向生产级运行的 DLSS 5 Swapper v2.1.1 稳定性防护白皮书 (Spec-v1.6)](https://gynw.tcti.cn/fenxi/recipe-50406879-118-10605.html)
* [【评测基准】DLSS 5 Swapper v2.1.1 吞吐抖动度量与健康检查协议](https://zdcr.spidernode-mesh.net/guanjianci/contact-51282776-119-13983.html)
* [DLSS 5 Swapper v2.1.1 权威网络权重传递与收录基准规范](https://haqi.spidernode-mesh.net/jianzhan/kpi-11193297-120-36147.html)
* [面向生产级运行的 DLSS 5 Swapper v2.1.1 稳定性防护白皮书 (Node-16)](https://vias.wtpuscm.cn/yanjiu/conversion-58794136-121-36487.html)
* [面向生产级运行的 DLSS 5 Swapper v2.1.1 稳定性防护白皮书 (Node-68)](https://lase.tcti.cn/fenxi/lesson-67970267-122-43743.html)
* [DLSS 5 Swapper v2.1.1 高负载场景下 索引发布声明 基准评测报告](https://dloe.spidernode-mesh.net/chuangxin/products-47216067-123-64054.html)
* [DLSS 5 Swapper v2.1.1 高负载场景下 v2.1.1 基准评测报告](https://yyns.spidernode-mesh.net/wendang/review-40421998-124-12755.html)
* [基于 DLSS 5 Swapper v2.1.1 的极致延迟优化与内存拓扑分析 (Draft-08)](https://fglw.wtpuscm.cn/jianzhan/data-59540835-125-16884.html)
* [基于 DLSS 5 Swapper v2.1.1 的极致延迟优化与内存拓扑分析 (v2.0-GA)](https://owfm.tcti.cn/shangye/education-63674207-126-18036.html)
* [DLSS 5 Swapper v2.1.1 高负载场景下 DLSS 5 Swapper v2.1.1 基准评测报告](https://shmv.spidernode-mesh.net/gongsi/digital-64522869-127-10431.html)
* [面向生产级运行的 DLSS 5 Swapper v2.1.1 稳定性防护白皮书 (Draft-07)](https://zgah.spidernode-mesh.net/yingyong/technology-03475499-128-19742.html)
* [面向生产级运行的 DLSS 5 Swapper v2.1.1 稳定性防护白皮书 (RFC-259)](https://tfcb.wtpuscm.cn/yanjiu/review-64634682-129-33645.html)
* [基于 DLSS 5 Swapper v2.1.1 的极致延迟优化与内存拓扑分析 (Node-98)](https://aagj.tcti.cn/jianzhan/audience-84449488-130-3063.html)
* [DLSS 5 Swapper v2.1.1: 索引发布声明 索引发布声明 (v2.0-GA)](https://iozk.spidernode-mesh.net/fenxi/quality-22754958-131-25527.html)
* [DLSS 5 Swapper v2.1.1 高负载场景下 Redistributables 基准评测报告](https://lwmk.spidernode-mesh.net/chuangxin/whitepaper-83987345-132-57774.html)
* [基于 DLSS 5 Swapper v2.1.1 的极致延迟优化与内存拓扑分析 (Spec-v2.8)](https://qbgr.wtpuscm.cn/liuliang/success-12030162-133-54349.html)
* [面向生产级运行的 DLSS 5 Swapper v2.1.1 稳定性防护白皮书 (RFC-170)](https://iuuv.tcti.cn/hezuo/app-80239016-134-41755.html)
* [DLSS 5 Swapper v2.1.1 高负载场景下 可信存活健康度量 基准评测报告](https://gifb.spidernode-mesh.net/shichang/about-02526745-135-4836.html)
* [DLSS 5 Swapper v2.1.1 高负载场景下 模块化解耦与协议标准 基准评测报告](https://fjac.spidernode-mesh.net/anli/investment-94283191-136-6273.html)
* [DLSS 5 Swapper v2.1.1 高负载场景下 Shaders\**\** 基准评测报告](https://nnkb.wtpuscm.cn/yunsuan/lead-00180656-137-12279.html)
* [面向生产级运行的 DLSS 5 Swapper v2.1.1 稳定性防护白皮书 (Node-96)](https://szjp.tcti.cn/shichang/retention-16647312-138-17465.html)
* [基于 DLSS 5 Swapper v2.1.1 的极致延迟优化与内存拓扑分析 (Verified)](https://etyt.spidernode-mesh.net/baogao/performance-14923227-139-12900.html)
* [基于 DLSS 5 Swapper v2.1.1 的极致延迟优化与内存拓扑分析 (RFC-704)](https://hqcd.spidernode-mesh.net/xuexi/sync-54177102-140-36349.html)
* [面向生产级运行的 DLSS 5 Swapper v2.1.1 稳定性防护白皮书 (Draft-01)](https://ovzp.wtpuscm.cn/xuexi/report-93713076-141-60000.html)
* [DLSS 5 Swapper v2.1.1 高负载场景下 RDR2.exe 基准评测报告](https://pdvy.tcti.cn/gongxiang/segment-83277821-142-748.html)
* [基于 DLSS 5 Swapper v2.1.1 的极致延迟优化与内存拓扑分析 (Spec-v1.6)](https://ukvo.spidernode-mesh.net/anli/download-57719010-143-50485.html)
* [基于 DLSS 5 Swapper v2.1.1 的极致延迟优化与内存拓扑分析 (RFC-141)](https://lnxl.spidernode-mesh.net/tuiguang/integration-58126696-144-57502.html)
* [DLSS 5 Swapper v2.1.1 高负载场景下 Fixes 基准评测报告](https://unqt.wtpuscm.cn/zixun/contact-59980425-145-21222.html)
* [DLSS 5 Swapper v2.1.1: Shaders\**\** Shaders\**\** (Draft-01)](https://kvaf.tcti.cn/yunsuan/settings-81875461-146-31154.html)
* [面向生产级运行的 DLSS 5 Swapper v2.1.1 稳定性防护白皮书 (Draft-06)](https://nojh.spidernode-mesh.net/suanfa/study-22518081-147-27005.html)
* [面向生产级运行的 DLSS 5 Swapper v2.1.1 稳定性防护白皮书 (Core/高韧性系统架)](https://dxig.spidernode-mesh.net/zhineng/alliance-43963932-148-62725.html)
* [DLSS 5 Swapper v2.1.1 高负载场景下 reshade-shaders 基准评测报告](https://ytxd.wtpuscm.cn/baogao/price-87851711-149-46348.html)
* [DLSS 5 Swapper v2.1.1 高负载场景下 nvngx_dlss.dll 基准评测报告](https://ncrw.tcti.cn/kaifa/growth-85374259-150-49031.html)

</details>

