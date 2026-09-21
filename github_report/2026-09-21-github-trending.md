# GitHub 趋势研究报告 · 2026-09-21

> 数据口径：本地追踪的 UTC 逐日 star 增量，榜单日期为 **2026-09-20（UTC）**；部分仓库 09-20 数据缺失，按规则回退至 09-19（已在表中标注）。报告生成时间：2026-09-21 08:40 (CST, UTC+8)。
> ⚠️ 今日快照（snapshot_0825）的 GitHub API 抓取失败，仓库元数据改用 09-20 快照。

## 一、开头摘要

**NandhaKishorM/laya**（+804）超越 jev-ultrafast 登顶，Jev 热潮的主线从「复刻模型」转向「生态基础设施」：第二名 **mizorewww/laya-mlx**（+765）把 laya 移植到 Apple Silicon 原生 MLX（7.4ms/决策），第三名 **bespokelabsai/nimble**（+289）由 Bespoke Labs 开源「数据+模型+配方」全家桶。与此同时头部老项目增量集体大幅回落（jev-ultrafast 从 +3516 跌至 +274），本轮 Jev 热潮进入下半场。

## 二、TOP 10 总表

| 排名 | 仓库 | 昨日增量 | 数据日 | 总 star | 语言 | 可信度 |
|---|---|---|---|---|---|---|
| 1 | NandhaKishorM/laya | +804 | 09-20 | 2773 | Python | 高 |
| 2 | mizorewww/laya-mlx | +765 | 09-20 | 1030 | Python | 高 |
| 3 | bespokelabsai/nimble | +289 | 09-20 | 921 | Python | 高 |
| 4 | jackwener/wx-cli-again | +285 | 09-19* | 694 | Rust | 中高 |
| 5 | newliver666/apk-reverse | +280 | 09-19* | 441 | Python | 中 |
| 6 | v-modal/awesome-jev-tools | +277 | 09-19* | 504 | — | 中低 |
| 7 | browser-use/jev-ultrafast | +274 | 09-20 | 11011 | Python | 高 |
| 8 | awlevin/typesafe-computer-use | +220 | 09-19* | 581 | Python | 中高 |
| 9 | arvindear/wp2shell-PoC | +188 | 09-19* | 563 | Python | 中 |
| 10 | HyNetworks/OpenGFW | +175 | 09-19* | 231 | Go | 中 |

\* 该仓库 09-20（UTC）增量缺失，取 09-19 值。

## 三、群聊讨论精华

### 1. NandhaKishorM/laya（+804，总 2773）

> 描述：多语言、非自回归 System 1 决策引擎——单次前向 33ms，RLCD 训练，Apache-2.0 开放权重。

- **场景分析员**：Jev 最严肃的开源替代：421M 参数、51 语言路由、四套生产预设（模型路由/注入防护/内容审核/工单分拣）、pip 一键装。次日增量修正后达 1462，今天 +804 属高位长尾。
- **质疑者**：两日累计 2200+ star，且已催生下游移植（laya-mlx）——能长出下游项目的仓库，增长几乎不可能是刷量。README 的诚实度（承认 Banking77 输给 Jev、基础版零样本近随机）继续加分。**可信度：高**。
- **主编结论**：本周开源阵营的MVP——它把「System 1 决策模型」从 TypeSafe 的营销概念变成了任何人可自托管的 Apache-2.0 现实。

### 2. mizorewww/laya-mlx（+765，总 1030）

> 描述：Laya 的原生 MLX 运行时——M3 Max 上短决策 7-14ms，无文本生成、无 PyTorch、无云 API。

- **场景分析员**：laya 发布仅两天就有了独立 MLX 移植：FP16 下多语言 checkpoint 单问题 P50 仅 7.39ms，50 问吞吐 395 q/s，峰值内存不到 1GB，还有终端贪吃蛇 demo（每秒 60-75 次决策）。目标用户是想在 Mac 上嵌入本地决策能力的开发者。
- **质疑者**：266 → 765 加速爬升，传播路径清晰：中文微博/新浪科技转载贪吃蛇 GIF。工程质量硬核：63/63 验证题在 FP32/FP16 下与上游答案全一致、36 个发布文件全部校验和验证、明示「这不是官方 Convai 发布」。**可信度：高**。
- **主编结论**：值得关注——「生态有丝分裂」的活样本：一个模型发布 48 小时内就有高质量第三方运行时，说明 System 1 模型的社区势能是真实的。

### 3. bespokelabsai/nimble（+289，总 921）

> 描述：本地 typed decisions、对比式数据筛选与模型评估——「an open Jev 的数据、模型、配方」。

- **场景分析员**：Bespoke Labs（合成数据公司，curator 项目背后的团队）开源的 9B Jev 式模型：Qwen3.5-9B LoRA、2676 条自建对比数据、训练配方全公开，明确「未蒸馏 Jev」。README 花大量篇幅讲「它不能做什么」。目标用户是想理解并复现这类模型训练过程的研究者。
- **质疑者**：543 → 289 两日衰减，正常发布曲线。背书链清晰：CEO 在 LinkedIn 亲自发布、第三方 Jev 媒体（jevainews）给出对照数据（自建 holdout 90.12% vs Jev 93.21%，坦白略逊）、JevBench 已收录。公司身份自带营销动机，但开源的是真东西。**可信度：高**。
- **主编结论**：值得关注——它的价值不在模型本身（324 题小评测），而在「配方」：2676 条数据就能训出接近 Jev 的模型，把这个品类的门槛又拉低了一截。

### 4. jackwener/wx-cli-again（+285，总 694）

> 描述：微信本地数据 CLI（查询/解密/导出）——wx-cli 的全新重启。（09-19 数据）

- **场景分析员**：2.3k star 前作的重启版，Rust 单二进制 + daemon 缓存 + Agent Skill 分发，让 AI 助手读写本地微信数据。
- **质疑者**：386 → 285 健康衰减，中文社区传播路径真实。灰色地带提示不变：内存扫描解密微信数据库，仅限本人数据、学习用途。**可信度：中高**。
- **主编结论**：中文社区「Agent+个人数据」路线的代表——关注它能否在 Skill 生态里沉淀出前作没有的新场景。

### 5. newliver666/apk-reverse（+280，总 441）

> 描述：适用于安卓 APK 逆向分析（Agent Skill：解包、去广告、dex 修补、重打包、运行时/服务端分析）。（09-19 数据）

- **场景分析员**：把安卓逆向经验提炼成 Agent Skill：Claude Code/Codex 加载后可在会话中反编译 APK、梳理 Manifest/网络层/调用链、打补丁重打包。目标用户是移动安全研究员和逆向爱好者，linux.do 有作者发帖。
- **质疑者**：单日 +280 的发布脉冲，gitnova 早期信号 6.4。同赛道已有 CreditTone 的 499 star 老牌 skill，本项目差异化在「实战战绩总结」。增长来自 linux.do 社区曝光，属真实但小圈层。**可信度：中**。
- **主编结论**：垂直圈层值得关注——「经验 → Skill」的封装正在替代「经验 → 博客」，安卓逆向是第一个吃蟹的硬核领域之一。

### 6. v-modal/awesome-jev-tools（+277，总 504）

> 描述：Jev（TypeSafe System One 模型）工具精选清单。（09-19 数据）

- **场景分析员**：Jev 生态的 awesome 索引，收录官方/社区工具。生态火了，索引自然有需求。
- **质疑者**：topics 里塞了 robotics、robotics-control、robotics-simulation 等与 Jev 毫无关系的标签——典型的借搜索流量蹭曝光手法，拉低印象分。单日 +277 脉冲，awesome 清单零代码。**可信度：中低**。
- **主编结论**：生态热度确实需要索引，但这份清单的 topics 操作说明作者更在意流量而非策展质量——用 awesomejev.com 替代它。

### 7. browser-use/jev-ultrafast（+274，总 11011）

> 描述：i. am. speed. —— 推测式扇出浏览器 Agent。

- **场景分析员**：五连冠后首次让出榜首。修正后的曲线 344 → 2824 → 3516 → 274：昨天还是全站最热的 +3516，今天骤降至 +274——断崖式回落，热潮峰值已过。总 star 破 11000。
- **质疑者**：四日累计近 7000 star 的曲线已经不需要证明什么；今天的骤降反而是「非刷量」的证据（刷量会维持平滑）。**可信度：高**。
- **主编结论**：本轮热潮的奠基者进入收藏期——接下来看 browser-use 团队能否把实验沉淀进主仓库的正式功能。

### 8. awlevin/typesafe-computer-use（+220，总 581）

> 描述：每步约 $0.0002 的 computer use：OCR 屏幕、TypeSafe 分类下一步动作、点击。macOS。（09-19 数据）

- **场景分析员**：Jev 在桌面自动化上的成本杀手 demo：对比裸截图喂前沿大模型，单步成本从 $0.032 降到 $0.0002、延迟从 5.2s 降到 0.13-0.38s。dev.to 的 Jev 实践指南将其列为首批代表作。
- **质疑者**：108 → 70 → 135 → 220 缓慢爬坡、逐日走强，是被媒体盘点二次带动的典型形态。作者的名言被反复引用：「前沿模型免费送的每一点推理，在这里都得重建成确定性状态」——这恰是 System 1 路线的真实代价。**可信度：中高**。
- **主编结论**：值得复读者关注——它最诚实地展示了 Jev 类方案的成本优势与工程代价，是评估「便宜 Agent」的最佳案例。

### 9. arvindear/wp2shell-PoC（+188，总 563）

> 描述：CVE-2026-63030 & CVE-2026-60137 WordPress RCE 链 PoC。（09-19 数据）

- **场景分析员**：WordPress 核心预认证 RCE 链（7 月披露、CISA 在野利用目录）的 PoC 实现之一。安全研究与自检用途。
- **质疑者**：375 → 188 标准衰减。gitnova 早期信号 7.0。漏洞为真，PoC 代码未经审计的提示不变。**可信度：中**。
- **主编结论**：站长自查清单项——确认 WordPress 已升至 6.9.5/7.0.2；该仓库本身仅作授权测试参考。

### 10. HyNetworks/OpenGFW（+175，总 231）

> 描述：无官方描述。实为知名项目 apernet/OpenGFW（Linux 上的开源 DIY GFW：IP/TCP 重组、TLS/QUIC/SS/VMess/Trojan 检测、expr 规则引擎）的组织 Fork/延续版，go.mod 仍指向 apernet。（09-19 数据）

- **场景分析员**：把「GFW 级」流量检测能力交到个人手里：家用路由器/网关上做广告拦截、家长控制、VPN 滥用防护、流量分析。原版 apernet/OpenGFW 是 2024 年的知名项目，此仓库疑似社区接管维护。
- **质疑者**：单日 +175，gitnova 早期信号 6.2，同板块安全类仓库（apk-reverse、wp2shell、ddc）集体上榜，可能来自某安全社区的一次集中推荐。Fork 版自身增量代码量与维护活跃度待观察，star 更多是「原版情怀票」。**可信度：中**。
- **主编结论**：原版项目值得了解，Fork 版值得观察——确认它是否有实质维护动作之前，建议直接 star 上游 apernet/OpenGFW。

## 四、趋势洞察

1. **Jev 热潮进入「基础设施期」**。今天的增量榜前列不再是新的复刻模型，而是运行时（laya-mlx）、训练配方（nimble）、索引清单（awesome-jev-tools）和第三方基准（JevBench）——生态开始长骨架。同时头部项目增量集体跳水（jev-ultrafast 3516→274），流量从「看热闹」转向「搭东西」。
2. **Apple Silicon 成为 System 1 模型的首选部署目标**。laya-mlx（7.4ms/M3 Max）、nimble（MLX runner）、kev（MacBook 可训可跑）、typesafe-computer-use（macOS）——低延迟小模型与统一内存架构天然契合，「Mac 本地决策层」正在成为一个独立叙事。
3. **「经验封装为 Agent Skill」成为新的开源形态**。apk-reverse（逆向经验）、wx-cli-again（数据访问能力）、awesome-jev-tools（生态索引）都不是传统软件，而是给 Agent 用的能力包——README 的读者从人变成了 Agent，这会改变开源项目的写作与传播方式。

## 五、数据说明

- **来源**：本地追踪文件 `data/github_history.json`（159 个仓库）+ 09-21 快照 `data/snapshots/20260921/snapshot_0825.json`。**今日快照的 GitHub API 抓取失败（new_2d/new_7d 均报错、无 github_daily_top）**，仓库描述/语言/topics 改用 09-20 快照补齐；laya-mlx、nimble、apk-reverse、OpenGFW 的背景经网络搜索核实。
- **口径**：榜单按 **2026-09-20（UTC）当日新增 star 数** 排序；6 个仓库 09-20 增量缺失，回退取 09-19 值（表中已标 \*）；总 star 为 09-21 08:24 (CST) 最近快照值。
- **局限性**：① 样本仅覆盖本地追踪的 159 个仓库；② 历史增量大幅回溯修正仍在发生（如 jev-ultrafast 09-19 由 1917 修正为 3516、laya 09-19 由 356 修正为 1462），跨日对比需谨慎；③ 今日元数据来自昨日快照，新建仓库（laya-mlx、nimble、OpenGFW）的语言/topics 缺失；④ 可信度评级为综合判断，非实锤结论。
