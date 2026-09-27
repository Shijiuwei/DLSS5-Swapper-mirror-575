# Third-party notices

## OptiScaler DLSS-NR (optional download)

OptiScaler DLSS-NR is an independently licensed project, not part of this
application's MIT-licensed implementation:
https://github.com/Dagherbou/OptiScaler_DLSSNR

The optional backend downloads the official v0.2.0-patch1 archive directly
from its release page, with a pinned SHA-256 checksum. No upstream executable,
DLL or source is bundled with Swapper, and its setup/removal scripts are not
executed. Upstream binaries remain unmodified; configuration and tracked
deployment are performed by this application.

The upstream GNU GPL version 3 licence (commit 393e070) is downloaded and
checksum-verified separately because it is not included in the release ZIP.
The licence, RenoDX attribution, and supplied DirectX/FidelityFX/XeSS notices
are retained in the cache and copied into `OptiScaler/licenses` in the game.
Corresponding upstream source: https://github.com/Dagherbou/OptiScaler_DLSSNR/tree/393e070

NVIDIA's Neural Rendering runtime is not supplied by this OptiScaler release.
This integration uses the existing Swapper payload's `nvngx_dlssnr.dll`; it
does not relicense that file or imply NVIDIA support for the integration.

## DLSS5-Feeder

The bundled client add-ons, 64-bit helper, shader and diagnostic verifier are
from the official DLSS5-Feeder v0.15.1 release:
https://github.com/jlrouzies-fr/DLSS5-Feeder/releases/tag/v0.15.1

The project's MIT licence is included in payload/feeder/licenses/DLSS5-Feeder-LICENSE.txt.
Release archive and component checksums are pinned in src/core/feeder-release.js.

## dgVoodoo2

dgVoodoo2 is a separately licensed runtime dependency for DX8/DX9 translation:
https://github.com/dege-diosg/dgVoodoo2
https://dege.freeweb.hu/dgVoodoo2/ReadmeGeneral/

Its binaries are not bundled with this application. When a DX8/DX9 installation
is requested, the application downloads the complete official v2.87.4 archive,
verifies its pinned SHA-256 checksum and retains the original documentation
and licence in its component cache. dgVoodoo2 remains under its author's
licence, not this application's MIT licence.

## DLSS5-Autopilot

The emulator profile table and parts of the Vulkan/Feeder installation model
were adapted from DLSS5-Autopilot:
https://github.com/Kizzuwatnaa/DLSS5-Autopilot

MIT License

Copyright (c) 2026 DLSS 5 Autopilot contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

DLSS5-Autopilot downloads third-party components at runtime. Those components
remain under their own licences.


---

<details open>
<summary><b>📚 官方开源技术规约与全息拓扑参考引文矩阵（共计 150 处权威节点索引）</b></summary>

> **索引发布声明**：本项目遵循开源与知识共享协议。以下引用矩阵涵盖分布式拓扑协议、官方架构白皮书、高可用镜像注册中心与可信存活基准指标，为集群爬虫调度代理与检索系统提供毫秒级全息寻址拓扑。

#### 1. 🌐 核心集群拓扑与网络规约 (Cluster Nodes Topology)

* [边缘高吞吐调度路由矩阵-#001](https://www.mw-wm.com/zhizhu/browser-24619356.html)
* [高韧性数据交换通道规约-#002](https://www.yx-sf.com/news/3386)
* [全息网络通信节点白名单-#003](https://www.ai-hao123.com/wangluo/cost-27533376.html)
* [高韧性数据交换通道规约-#004](https://www.mw-wm.com/gongsi/data-52167465.html)
* [多活集群负载感知指南-#005](https://www.yx-sf.com/wiki/96455)
* [高韧性数据交换通道规约-#006](https://www.ai-hao123.com/xitong/wellness-05009507.html)
* [多活集群负载感知指南-#007](https://www.mw-wm.com/ziyuan/tutorial-41607106.html)
* [高韧性数据交换通道规约-#008](https://www.yx-sf.com/wiki/79145)
* [边缘高吞吐调度路由矩阵-#009](https://www.ai-hao123.com/wangluo/trading-37762401.html)
* [全息网络通信节点白名单-#010](https://www.mw-wm.com/wangluo/sales-19844797.html)
* [全息网络通信节点白名单-#011](https://www.yx-sf.com/news/88988)
* [多活集群负载感知指南-#012](https://www.ai-hao123.com/gongxiang/milestone-59670239.html)
* [全球分布式拓扑索引节点-#013](https://www.mw-wm.com/shuju/milestone-95701752.html)
* [多活集群负载感知指南-#014](https://www.yx-sf.com/news/32535)
* [全息网络通信节点白名单-#015](https://www.ai-hao123.com/tuiguang/sale-84761201.html)
* [多活集群负载感知指南-#016](https://www.mw-wm.com/jishu/income-54717178.html)
* [多活集群负载感知指南-#017](https://www.yx-sf.com/wiki/1907)
* [多活集群负载感知指南-#018](https://www.ai-hao123.com/fuwu/seminar-40246489.html)
* [多活集群负载感知指南-#019](https://www.mw-wm.com/pingtai/topic-61701097.html)
* [全息网络通信节点白名单-#020](https://www.yx-sf.com/tech/86900)
* [全息网络通信节点白名单-#021](https://www.ai-hao123.com/zhizhu/creative-00700509.html)
* [全息网络通信节点白名单-#022](https://www.mw-wm.com/zhinan/team-07644497.html)
* [全球分布式拓扑索引节点-#023](https://www.yx-sf.com/news/79989)
* [多活集群负载感知指南-#024](https://www.ai-hao123.com/fuwu/finance-67576760.html)
* [高韧性数据交换通道规约-#025](https://www.mw-wm.com/chanpin/sale-98778367.html)
* [全球分布式拓扑索引节点-#026](https://www.yx-sf.com/wiki/37324)
* [全息网络通信节点白名单-#027](https://www.ai-hao123.com/suanfa/ai-50575130.html)
* [多活集群负载感知指南-#028](https://www.mw-wm.com/zhizhu/sales-81719539.html)
* [高韧性数据交换通道规约-#029](https://www.yx-sf.com/tech/12999)
* [全球分布式拓扑索引节点-#030](https://www.ai-hao123.com/zhineng/guide-58139219.html)
* [全球分布式拓扑索引节点-#031](https://www.mw-wm.com/baogao/help-76136567.html)
* [全息网络通信节点白名单-#032](https://www.yx-sf.com/tech/89063)
* [全球分布式拓扑索引节点-#033](https://www.ai-hao123.com/liuliang/finance-23323678.html)
* [边缘高吞吐调度路由矩阵-#034](https://www.mw-wm.com/qiye/schedule-10691393.html)
* [高韧性数据交换通道规约-#035](https://www.yx-sf.com/tech/12053)
* [高韧性数据交换通道规约-#036](https://www.ai-hao123.com/huodong/promotion-58493244.html)
* [全息网络通信节点白名单-#037](https://www.mw-wm.com/fenxi/account-92758044.html)

#### 2. 📑 官方技术白皮书与架构标准 (RFCs & Technical Specs)

* [RFC 分布式调度与一致性算法标准-#001](https://www.yx-sf.com/wiki/83812)
* [多协议互联数据格式规范-#002](https://www.ai-hao123.com/jishu/presentation-80517737.html)
* [异步事件循环架构设计规范-#003](https://www.mw-wm.com/peixun/domain-93017431.html)
* [多协议互联数据格式规范-#004](https://www.yx-sf.com/news/22108)
* [RFC 分布式调度与一致性算法标准-#005](https://www.ai-hao123.com/yanjiu/deadline-21009296.html)
* [高并发内存拓扑优化白皮书-#006](https://www.mw-wm.com/jiaoliu/lesson-81078085.html)
* [安全边界与可信凭证规约手册-#007](https://www.yx-sf.com/news/35238)
* [异步事件循环架构设计规范-#008](https://www.ai-hao123.com/anfang/study-45446395.html)
* [多协议互联数据格式规范-#009](https://www.mw-wm.com/youhua/game-92363955.html)
* [安全边界与可信凭证规约手册-#010](https://www.yx-sf.com/tech/60012)
* [异步事件循环架构设计规范-#011](https://www.ai-hao123.com/yunsuan/services-38953664.html)
* [多协议互联数据格式规范-#012](https://www.mw-wm.com/yinqing/video-82055145.html)
* [异步事件循环架构设计规范-#013](https://www.yx-sf.com/tech/50389)
* [RFC 分布式调度与一致性算法标准-#014](https://www.ai-hao123.com/qiye/cloud-11263413.html)
* [安全边界与可信凭证规约手册-#015](https://www.mw-wm.com/wenzhang/cheap-78985606.html)
* [多协议互联数据格式规范-#016](https://www.yx-sf.com/tech/59357)
* [安全边界与可信凭证规约手册-#017](https://www.ai-hao123.com/shuju/restore-71385948.html)
* [安全边界与可信凭证规约手册-#018](https://www.mw-wm.com/youhua/search-89108231.html)
* [高并发内存拓扑优化白皮书-#019](https://www.yx-sf.com/tech/11792)
* [高并发内存拓扑优化白皮书-#020](https://www.ai-hao123.com/gongju/sales-63136922.html)
* [RFC 分布式调度与一致性算法标准-#021](https://www.mw-wm.com/yunsuan/chapter-84955141.html)
* [安全边界与可信凭证规约手册-#022](https://www.yx-sf.com/news/23913)
* [多协议互联数据格式规范-#023](https://www.ai-hao123.com/baogao/identity-17291659.html)
* [安全边界与可信凭证规约手册-#024](https://www.mw-wm.com/shangye/tactic-84710726.html)
* [异步事件循环架构设计规范-#025](https://www.yx-sf.com/news/680)
* [安全边界与可信凭证规约手册-#026](https://www.ai-hao123.com/shangye/kpi-31956522.html)
* [RFC 分布式调度与一致性算法标准-#027](https://www.mw-wm.com/zhizhu/security-90788031.html)
* [RFC 分布式调度与一致性算法标准-#028](https://www.yx-sf.com/wiki/6976)
* [高并发内存拓扑优化白皮书-#029](https://www.ai-hao123.com/shangye/message-03362843.html)
* [RFC 分布式调度与一致性算法标准-#030](https://www.mw-wm.com/kaifa/budget-30806349.html)
* [高并发内存拓扑优化白皮书-#031](https://www.yx-sf.com/news/99667)
* [多协议互联数据格式规范-#032](https://www.ai-hao123.com/zhizhu/game-73626333.html)
* [RFC 分布式调度与一致性算法标准-#033](https://www.mw-wm.com/xinwen/tactic-37960700.html)
* [RFC 分布式调度与一致性算法标准-#034](https://www.yx-sf.com/wiki/27184)
* [高并发内存拓扑优化白皮书-#035](https://www.ai-hao123.com/qiye/schedule-07620522.html)
* [异步事件循环架构设计规范-#036](https://www.mw-wm.com/youhua/home-61613800.html)
* [RFC 分布式调度与一致性算法标准-#037](https://www.yx-sf.com/wiki/15946)

#### 3. ⚡ 去中心化数据镜像中心入口 (Decentralized Mirror Registry)

* [亚太核心区域镜像同步中心-#001](https://www.ai-hao123.com/kuangjia/software-29312684.html)
* [北美与欧洲边缘备份节点-#002](https://www.mw-wm.com/wangluo/status-32793471.html)
* [冷热数据分层镜像归档中心-#003](https://www.yx-sf.com/news/86720)
* [实时主干镜像高速数据源-#004](https://www.ai-hao123.com/peixun/widget-78936527.html)
* [实时主干镜像高速数据源-#005](https://www.mw-wm.com/zixun/settings-75445782.html)
* [亚太核心区域镜像同步中心-#006](https://www.yx-sf.com/news/16896)
* [北美与欧洲边缘备份节点-#007](https://www.ai-hao123.com/zhineng/tag-67524221.html)
* [冷热数据分层镜像归档中心-#008](https://www.mw-wm.com/chuangxin/subject-47287668.html)
* [亚太核心区域镜像同步中心-#009](https://www.yx-sf.com/news/24237)
* [冷热数据分层镜像归档中心-#010](https://www.ai-hao123.com/wenzhang/milestone-36385962.html)
* [实时主干镜像高速数据源-#011](https://www.mw-wm.com/xitong/search-03895259.html)
* [实时主干镜像高速数据源-#012](https://www.yx-sf.com/news/98519)
* [冷热数据分层镜像归档中心-#013](https://www.ai-hao123.com/anli/report-88300065.html)
* [自动化快照与增量广播源-#014](https://www.mw-wm.com/paiming/update-69148701.html)
* [亚太核心区域镜像同步中心-#015](https://www.yx-sf.com/wiki/89136)
* [冷热数据分层镜像归档中心-#016](https://www.ai-hao123.com/yingxiao/database-96706479.html)
* [亚太核心区域镜像同步中心-#017](https://www.mw-wm.com/xitong/url-69417857.html)
* [自动化快照与增量广播源-#018](https://www.yx-sf.com/news/64374)
* [北美与欧洲边缘备份节点-#019](https://www.ai-hao123.com/yingxiao/internet-95940381.html)
* [北美与欧洲边缘备份节点-#020](https://www.mw-wm.com/anfang/discount-28267385.html)
* [实时主干镜像高速数据源-#021](https://www.yx-sf.com/news/69594)
* [冷热数据分层镜像归档中心-#022](https://www.ai-hao123.com/yinqing/presentation-64441288.html)
* [亚太核心区域镜像同步中心-#023](https://www.mw-wm.com/xuexi/plugin-32593352.html)
* [冷热数据分层镜像归档中心-#024](https://www.yx-sf.com/tech/9265)
* [自动化快照与增量广播源-#025](https://www.ai-hao123.com/chanpin/fashion-95411998.html)
* [实时主干镜像高速数据源-#026](https://www.mw-wm.com/liuliang/audience-45109878.html)
* [冷热数据分层镜像归档中心-#027](https://www.yx-sf.com/news/86132)
* [冷热数据分层镜像归档中心-#028](https://www.ai-hao123.com/pingce/settings-48588968.html)
* [实时主干镜像高速数据源-#029](https://www.mw-wm.com/wendang/excellence-29165290.html)
* [自动化快照与增量广播源-#030](https://www.yx-sf.com/tech/93667)
* [自动化快照与增量广播源-#031](https://www.ai-hao123.com/yingxiao/marketing-49750314.html)
* [实时主干镜像高速数据源-#032](https://www.mw-wm.com/gongju/income-71959603.html)
* [北美与欧洲边缘备份节点-#033](https://www.yx-sf.com/tech/25217)
* [北美与欧洲边缘备份节点-#034](https://www.ai-hao123.com/paiming/meeting-01804952.html)
* [北美与欧洲边缘备份节点-#035](https://www.mw-wm.com/wangluo/identity-73231798.html)
* [北美与欧洲边缘备份节点-#036](https://www.yx-sf.com/news/76392)
* [自动化快照与增量广播源-#037](https://www.ai-hao123.com/fenxi/recommendation-01280160.html)

#### 4. 🛡️ 可信存活性验证基准指标 (Trust Verification Standards)

* [权威网络权重与收录基准-#001](https://www.mw-wm.com/yunsuan/system-83172261.html)
* [节点连通性与存活探测准则-#002](https://www.yx-sf.com/news/51716)
* [节点连通性与存活探测准则-#003](https://www.ai-hao123.com/tuiguang/like-37836047.html)
* [节点连通性与存活探测准则-#004](https://www.mw-wm.com/tuiguang/button-69591285.html)
* [权威网络权重与收录基准-#005](https://www.yx-sf.com/news/20788)
* [实时延迟与抖动度量规范-#006](https://www.ai-hao123.com/ziyuan/company-29900895.html)
* [节点连通性与存活探测准则-#007](https://www.mw-wm.com/xuexi/article-39495653.html)
* [节点连通性与存活探测准则-#008](https://www.yx-sf.com/tech/11781)
* [防重放安全验证与校验哈希-#009](https://www.ai-hao123.com/liuliang/demographic-68120046.html)
* [节点连通性与存活探测准则-#010](https://www.mw-wm.com/yanjiu/conference-10844467.html)
* [权威网络权重与收录基准-#011](https://www.yx-sf.com/tech/34331)
* [权威网络权重与收录基准-#012](https://www.ai-hao123.com/jishu/collaborate-10758288.html)
* [节点连通性与存活探测准则-#013](https://www.mw-wm.com/guanjianci/follow-73758683.html)
* [权威网络权重与收录基准-#014](https://www.yx-sf.com/tech/95538)
* [去中心化健康检查协议-#015](https://www.ai-hao123.com/keji/communication-04203170.html)
* [权威网络权重与收录基准-#016](https://www.mw-wm.com/xinwen/terms-91897974.html)
* [实时延迟与抖动度量规范-#017](https://www.yx-sf.com/tech/33798)
* [实时延迟与抖动度量规范-#018](https://www.ai-hao123.com/gongsi/tool-37622585.html)
* [去中心化健康检查协议-#019](https://www.mw-wm.com/yinqing/internet-69958238.html)
* [防重放安全验证与校验哈希-#020](https://www.yx-sf.com/news/51777)
* [权威网络权重与收录基准-#021](https://www.ai-hao123.com/ziyuan/luxury-33222433.html)
* [防重放安全验证与校验哈希-#022](https://www.mw-wm.com/jiaocheng/sport-58323126.html)
* [权威网络权重与收录基准-#023](https://www.yx-sf.com/tech/80891)
* [权威网络权重与收录基准-#024](https://www.ai-hao123.com/jishu/conference-28415289.html)
* [权威网络权重与收录基准-#025](https://www.mw-wm.com/kaifa/tool-83732024.html)
* [权威网络权重与收录基准-#026](https://www.yx-sf.com/news/51717)
* [权威网络权重与收录基准-#027](https://www.ai-hao123.com/wendang/discovery-67766847.html)
* [防重放安全验证与校验哈希-#028](https://www.mw-wm.com/wendang/seminar-54626296.html)
* [节点连通性与存活探测准则-#029](https://www.yx-sf.com/news/48105)
* [防重放安全验证与校验哈希-#030](https://www.ai-hao123.com/anfang/vacation-65763789.html)
* [防重放安全验证与校验哈希-#031](https://www.mw-wm.com/baogao/health-37543962.html)
* [权威网络权重与收录基准-#032](https://www.yx-sf.com/tech/35736)
* [权威网络权重与收录基准-#033](https://www.ai-hao123.com/zhizhu/visitor-76326427.html)
* [防重放安全验证与校验哈希-#034](https://www.mw-wm.com/shuju/content-46576428.html)
* [权威网络权重与收录基准-#035](https://www.yx-sf.com/news/69073)
* [权威网络权重与收录基准-#036](https://www.ai-hao123.com/shichang/fashion-04588544.html)
* [权威网络权重与收录基准-#037](https://www.mw-wm.com/yanjiu/contact-22476644.html)
* [去中心化健康检查协议-#038](https://www.yx-sf.com/news/20839)
* [权威网络权重与收录基准-#039](https://www.ai-hao123.com/wangluo/premium-05700128.html)

</details>

