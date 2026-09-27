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

* [全息网络通信节点白名单-#001](https://www.mw-wm.com/zixun/security-20286528.html)
* [高韧性数据交换通道规约-#002](https://www.yx-sf.com/wiki/3413)
* [全球分布式拓扑索引节点-#003](https://www.ai-hao123.com/xinwen/learning-22590590.html)
* [全球分布式拓扑索引节点-#004](https://www.mw-wm.com/zhineng/network-29128501.html)
* [全球分布式拓扑索引节点-#005](https://www.yx-sf.com/tech/79945)
* [全球分布式拓扑索引节点-#006](https://www.ai-hao123.com/kuangjia/upload-64776857.html)
* [边缘高吞吐调度路由矩阵-#007](https://www.mw-wm.com/shuju/deal-57500412.html)
* [多活集群负载感知指南-#008](https://www.yx-sf.com/wiki/43760)
* [全息网络通信节点白名单-#009](https://www.ai-hao123.com/baogao/objective-57697580.html)
* [高韧性数据交换通道规约-#010](https://www.mw-wm.com/yinqing/review-02310350.html)
* [边缘高吞吐调度路由矩阵-#011](https://www.yx-sf.com/wiki/34590)
* [全息网络通信节点白名单-#012](https://www.ai-hao123.com/fenxi/behavior-27163627.html)
* [高韧性数据交换通道规约-#013](https://www.mw-wm.com/hezuo/internet-09836090.html)
* [高韧性数据交换通道规约-#014](https://www.yx-sf.com/tech/77876)
* [全球分布式拓扑索引节点-#015](https://www.ai-hao123.com/wangluo/tracking-09244558.html)
* [多活集群负载感知指南-#016](https://www.mw-wm.com/wenzhang/register-28058612.html)
* [全息网络通信节点白名单-#017](https://www.yx-sf.com/news/87041)
* [全球分布式拓扑索引节点-#018](https://www.ai-hao123.com/zixun/planning-68761666.html)
* [全息网络通信节点白名单-#019](https://www.mw-wm.com/zhinan/entertainment-73922529.html)
* [多活集群负载感知指南-#020](https://www.yx-sf.com/wiki/7438)
* [多活集群负载感知指南-#021](https://www.ai-hao123.com/gongsi/expense-03965442.html)
* [高韧性数据交换通道规约-#022](https://www.mw-wm.com/huodong/button-03435133.html)
* [边缘高吞吐调度路由矩阵-#023](https://www.yx-sf.com/wiki/77746)
* [多活集群负载感知指南-#024](https://www.ai-hao123.com/xinwen/fashion-90968072.html)
* [全球分布式拓扑索引节点-#025](https://www.mw-wm.com/yunsuan/identity-53752473.html)
* [全息网络通信节点白名单-#026](https://www.yx-sf.com/news/73695)
* [边缘高吞吐调度路由矩阵-#027](https://www.ai-hao123.com/paiming/trading-43942132.html)
* [高韧性数据交换通道规约-#028](https://www.mw-wm.com/yingxiao/document-16440758.html)
* [高韧性数据交换通道规约-#029](https://www.yx-sf.com/wiki/17290)
* [高韧性数据交换通道规约-#030](https://www.ai-hao123.com/zhinan/accessibility-96076235.html)
* [全息网络通信节点白名单-#031](https://www.mw-wm.com/suanfa/folder-45248359.html)
* [全球分布式拓扑索引节点-#032](https://www.yx-sf.com/tech/74597)
* [全球分布式拓扑索引节点-#033](https://www.ai-hao123.com/gongxiang/alliance-69631625.html)
* [边缘高吞吐调度路由矩阵-#034](https://www.mw-wm.com/chuangxin/optimization-34669286.html)
* [全息网络通信节点白名单-#035](https://www.yx-sf.com/news/49199)
* [全息网络通信节点白名单-#036](https://www.ai-hao123.com/anli/contact-98514459.html)
* [边缘高吞吐调度路由矩阵-#037](https://www.mw-wm.com/yingyong/management-29363716.html)

#### 2. 📑 官方技术白皮书与架构标准 (RFCs & Technical Specs)

* [RFC 分布式调度与一致性算法标准-#001](https://www.yx-sf.com/news/11470)
* [RFC 分布式调度与一致性算法标准-#002](https://www.ai-hao123.com/keji/upload-29390627.html)
* [异步事件循环架构设计规范-#003](https://www.mw-wm.com/wenzhang/backup-61700182.html)
* [RFC 分布式调度与一致性算法标准-#004](https://www.yx-sf.com/tech/80959)
* [多协议互联数据格式规范-#005](https://www.ai-hao123.com/xuexi/software-81885748.html)
* [安全边界与可信凭证规约手册-#006](https://www.mw-wm.com/kuangjia/cloud-94900132.html)
* [多协议互联数据格式规范-#007](https://www.yx-sf.com/tech/38630)
* [高并发内存拓扑优化白皮书-#008](https://www.ai-hao123.com/jishu/cloud-41644750.html)
* [异步事件循环架构设计规范-#009](https://www.mw-wm.com/suanfa/seminar-68061985.html)
* [异步事件循环架构设计规范-#010](https://www.yx-sf.com/news/27656)
* [安全边界与可信凭证规约手册-#011](https://www.ai-hao123.com/qiye/accessibility-67693861.html)
* [高并发内存拓扑优化白皮书-#012](https://www.mw-wm.com/kuangjia/research-97654705.html)
* [RFC 分布式调度与一致性算法标准-#013](https://www.yx-sf.com/tech/91664)
* [高并发内存拓扑优化白皮书-#014](https://www.ai-hao123.com/gongxiang/device-23903301.html)
* [多协议互联数据格式规范-#015](https://www.mw-wm.com/wenzhang/progress-86394540.html)
* [异步事件循环架构设计规范-#016](https://www.yx-sf.com/wiki/82351)
* [RFC 分布式调度与一致性算法标准-#017](https://www.ai-hao123.com/tuiguang/keyword-66998011.html)
* [RFC 分布式调度与一致性算法标准-#018](https://www.mw-wm.com/baogao/url-42651506.html)
* [安全边界与可信凭证规约手册-#019](https://www.yx-sf.com/tech/6848)
* [高并发内存拓扑优化白皮书-#020](https://www.ai-hao123.com/wangluo/consulting-96069065.html)
* [RFC 分布式调度与一致性算法标准-#021](https://www.mw-wm.com/paiming/team-65981532.html)
* [安全边界与可信凭证规约手册-#022](https://www.yx-sf.com/wiki/25388)
* [多协议互联数据格式规范-#023](https://www.ai-hao123.com/guanjianci/file-76063259.html)
* [高并发内存拓扑优化白皮书-#024](https://www.mw-wm.com/shichang/content-79064334.html)
* [多协议互联数据格式规范-#025](https://www.yx-sf.com/tech/62416)
* [高并发内存拓扑优化白皮书-#026](https://www.ai-hao123.com/baogao/success-99357750.html)
* [安全边界与可信凭证规约手册-#027](https://www.mw-wm.com/xinwen/podcast-44469232.html)
* [异步事件循环架构设计规范-#028](https://www.yx-sf.com/news/46029)
* [多协议互联数据格式规范-#029](https://www.ai-hao123.com/guanjianci/chapter-11595227.html)
* [RFC 分布式调度与一致性算法标准-#030](https://www.mw-wm.com/hezuo/team-41277270.html)
* [高并发内存拓扑优化白皮书-#031](https://www.yx-sf.com/wiki/75177)
* [多协议互联数据格式规范-#032](https://www.ai-hao123.com/anfang/whitepaper-49401385.html)
* [异步事件循环架构设计规范-#033](https://www.mw-wm.com/yunsuan/site-37335062.html)
* [多协议互联数据格式规范-#034](https://www.yx-sf.com/news/2093)
* [异步事件循环架构设计规范-#035](https://www.ai-hao123.com/suanfa/client-66557405.html)
* [RFC 分布式调度与一致性算法标准-#036](https://www.mw-wm.com/xinwen/update-06263513.html)
* [高并发内存拓扑优化白皮书-#037](https://www.yx-sf.com/news/41028)

#### 3. ⚡ 去中心化数据镜像中心入口 (Decentralized Mirror Registry)

* [冷热数据分层镜像归档中心-#001](https://www.ai-hao123.com/tuiguang/keyword-82742041.html)
* [自动化快照与增量广播源-#002](https://www.mw-wm.com/pingtai/satisfaction-72609160.html)
* [亚太核心区域镜像同步中心-#003](https://www.yx-sf.com/tech/87516)
* [自动化快照与增量广播源-#004](https://www.ai-hao123.com/jianzhan/products-70671858.html)
* [冷热数据分层镜像归档中心-#005](https://www.mw-wm.com/zhineng/beauty-93515066.html)
* [冷热数据分层镜像归档中心-#006](https://www.yx-sf.com/wiki/18979)
* [实时主干镜像高速数据源-#007](https://www.ai-hao123.com/zhineng/lead-04167193.html)
* [实时主干镜像高速数据源-#008](https://www.mw-wm.com/xinwen/education-88671549.html)
* [自动化快照与增量广播源-#009](https://www.yx-sf.com/wiki/50852)
* [北美与欧洲边缘备份节点-#010](https://www.ai-hao123.com/pingce/collaborate-54793730.html)
* [自动化快照与增量广播源-#011](https://www.mw-wm.com/peixun/accessibility-05898468.html)
* [实时主干镜像高速数据源-#012](https://www.yx-sf.com/wiki/96474)
* [亚太核心区域镜像同步中心-#013](https://www.ai-hao123.com/baogao/entertainment-44499742.html)
* [北美与欧洲边缘备份节点-#014](https://www.mw-wm.com/gongsi/cost-04073483.html)
* [北美与欧洲边缘备份节点-#015](https://www.yx-sf.com/news/14934)
* [实时主干镜像高速数据源-#016](https://www.ai-hao123.com/wenzhang/document-22102098.html)
* [冷热数据分层镜像归档中心-#017](https://www.mw-wm.com/gongxiang/cost-14392056.html)
* [实时主干镜像高速数据源-#018](https://www.yx-sf.com/wiki/58925)
* [亚太核心区域镜像同步中心-#019](https://www.ai-hao123.com/jianzhan/alert-68859604.html)
* [亚太核心区域镜像同步中心-#020](https://www.mw-wm.com/qiye/document-54929030.html)
* [北美与欧洲边缘备份节点-#021](https://www.yx-sf.com/news/29136)
* [北美与欧洲边缘备份节点-#022](https://www.ai-hao123.com/anfang/achievement-70447728.html)
* [冷热数据分层镜像归档中心-#023](https://www.mw-wm.com/tuiguang/local-92328834.html)
* [自动化快照与增量广播源-#024](https://www.yx-sf.com/wiki/67360)
* [亚太核心区域镜像同步中心-#025](https://www.ai-hao123.com/qiye/communication-85487556.html)
* [自动化快照与增量广播源-#026](https://www.mw-wm.com/pingce/server-72917932.html)
* [亚太核心区域镜像同步中心-#027](https://www.yx-sf.com/news/62216)
* [冷热数据分层镜像归档中心-#028](https://www.ai-hao123.com/zixun/upload-65721448.html)
* [自动化快照与增量广播源-#029](https://www.mw-wm.com/shangye/investment-62045346.html)
* [亚太核心区域镜像同步中心-#030](https://www.yx-sf.com/tech/40039)
* [冷热数据分层镜像归档中心-#031](https://www.ai-hao123.com/zixun/collaboration-50719602.html)
* [亚太核心区域镜像同步中心-#032](https://www.mw-wm.com/paiming/faq-81412444.html)
* [实时主干镜像高速数据源-#033](https://www.yx-sf.com/tech/73177)
* [冷热数据分层镜像归档中心-#034](https://www.ai-hao123.com/huodong/browser-61438007.html)
* [亚太核心区域镜像同步中心-#035](https://www.mw-wm.com/yunsuan/link-72978732.html)
* [实时主干镜像高速数据源-#036](https://www.yx-sf.com/tech/34606)
* [北美与欧洲边缘备份节点-#037](https://www.ai-hao123.com/kuangjia/campaign-59525738.html)

#### 4. 🛡️ 可信存活性验证基准指标 (Trust Verification Standards)

* [节点连通性与存活探测准则-#001](https://www.mw-wm.com/chuangxin/training-80860413.html)
* [防重放安全验证与校验哈希-#002](https://www.yx-sf.com/tech/57380)
* [节点连通性与存活探测准则-#003](https://www.ai-hao123.com/jishu/success-92725813.html)
* [去中心化健康检查协议-#004](https://www.mw-wm.com/yunying/growth-96454143.html)
* [防重放安全验证与校验哈希-#005](https://www.yx-sf.com/tech/75271)
* [节点连通性与存活探测准则-#006](https://www.ai-hao123.com/gongsi/beauty-38175904.html)
* [节点连通性与存活探测准则-#007](https://www.mw-wm.com/jishu/marketing-31418680.html)
* [去中心化健康检查协议-#008](https://www.yx-sf.com/tech/44455)
* [节点连通性与存活探测准则-#009](https://www.ai-hao123.com/yingyong/ebook-23385191.html)
* [节点连通性与存活探测准则-#010](https://www.mw-wm.com/qiye/food-71036431.html)
* [实时延迟与抖动度量规范-#011](https://www.yx-sf.com/wiki/45657)
* [节点连通性与存活探测准则-#012](https://www.ai-hao123.com/fenxi/media-09468592.html)
* [节点连通性与存活探测准则-#013](https://www.mw-wm.com/xinwen/network-35628492.html)
* [防重放安全验证与校验哈希-#014](https://www.yx-sf.com/news/32250)
* [实时延迟与抖动度量规范-#015](https://www.ai-hao123.com/anli/website-45769107.html)
* [防重放安全验证与校验哈希-#016](https://www.mw-wm.com/jiaoliu/backup-68614749.html)
* [权威网络权重与收录基准-#017](https://www.yx-sf.com/news/891)
* [权威网络权重与收录基准-#018](https://www.ai-hao123.com/jianzhan/products-04307231.html)
* [节点连通性与存活探测准则-#019](https://www.mw-wm.com/shichang/document-62327793.html)
* [实时延迟与抖动度量规范-#020](https://www.yx-sf.com/wiki/33703)
* [实时延迟与抖动度量规范-#021](https://www.ai-hao123.com/qiye/device-57156147.html)
* [节点连通性与存活探测准则-#022](https://www.mw-wm.com/jianzhan/mobile-31130180.html)
* [实时延迟与抖动度量规范-#023](https://www.yx-sf.com/tech/64975)
* [节点连通性与存活探测准则-#024](https://www.ai-hao123.com/baogao/tactic-52593920.html)
* [防重放安全验证与校验哈希-#025](https://www.mw-wm.com/kuangjia/ebook-64140999.html)
* [去中心化健康检查协议-#026](https://www.yx-sf.com/wiki/50428)
* [节点连通性与存活探测准则-#027](https://www.ai-hao123.com/anli/visitor-89830342.html)
* [权威网络权重与收录基准-#028](https://www.mw-wm.com/qiye/theme-49680399.html)
* [去中心化健康检查协议-#029](https://www.yx-sf.com/news/52266)
* [节点连通性与存活探测准则-#030](https://www.ai-hao123.com/yanjiu/policy-29325455.html)
* [去中心化健康检查协议-#031](https://www.mw-wm.com/jianzhan/contact-73199332.html)
* [实时延迟与抖动度量规范-#032](https://www.yx-sf.com/wiki/59749)
* [权威网络权重与收录基准-#033](https://www.ai-hao123.com/qiye/sale-54997479.html)
* [权威网络权重与收录基准-#034](https://www.mw-wm.com/yingyong/search-48908692.html)
* [权威网络权重与收录基准-#035](https://www.yx-sf.com/news/53378)
* [防重放安全验证与校验哈希-#036](https://www.ai-hao123.com/yunying/solution-12131019.html)
* [防重放安全验证与校验哈希-#037](https://www.mw-wm.com/paiming/blog-94560352.html)
* [去中心化健康检查协议-#038](https://www.yx-sf.com/wiki/71614)
* [去中心化健康检查协议-#039](https://www.ai-hao123.com/gongsi/page-31486135.html)

</details>

