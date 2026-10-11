# GitHub 趋势研究报告 · 2026-10-10

> 榜单数据日期：**2026-10-09（UTC）**，口径为逐日真实 star 增量（非当日 trending 榜）。本期原始 TOP 20 中混入了 10 个同日批量创建的盗版软件刷量仓库，已识别并剔除，正文按剔除后排名呈现。

---

## 一、开头摘要

今天有两条主线。第一条是**「AI 重写桌面软件」运动正式成军**：ArtCraft 团队的 Craft 系列（Word/Excel/AutoCAD/PowerPoint 的纯 Rust 净室重写，全部内置 MCP 接口供 AI Agent 驱动）四个仓库同时进入 TOP 10，配合 nullmoth 的 NVIDIA macOS 驱动（RTX 5060 在 macOS 上跑起 Metal 3，VideoCardz 已报道），「AI 辅助逆向 + 净室重写」正在从单点实验变成批量生产线。第二条是警报：**一个 warez 刷量农场在 10 月 9 日 13:44–13:59 的 15 分钟内批量创建了至少 10 个盗版软件诱饵仓库**（KMS-Pico、Total-Commander、Better-Discord 等），同日各刷 400–614 star，已占据原始榜单半壁江山——GitHub 正被这类投毒农场系统性渗透，本期已全部剔除并在文末列出。

---

## 二、TOP 10 总表（已剔除刷量农场）

| 排名 | 仓库 | 昨日增量 | 总 star | 语言 | 可信度 |
|---:|---|---:|---:|---|:--:|
| 1 | mhtsec/ARTEX | +972 | 2,333 | Go | 中 |
| 2 | storytold/wordcraft | +957 | 1,987 | Rust | 中高 |
| 3 | LosaLosSantos/aurelio-finance | +855 | 1,556 | Python | 中高 |
| 4 | openai/math | +683 | 13,164 | Lean | 高 |
| 5 | zhongerxin/iPhone-use | +623 | 1,949 | Python | 高 |
| 6 | storytold/gridcraft | +563 | 1,245 | Rust | 中高 |
| 7 | noahdunnagan/fsearch | +513 | 1,218 | Rust | 中高 |
| 8 | nullmoth/nvidia-macos-driver | +490 | 1,943 | Rust | 高 |
| 9 | storytold/cadcraft | +478 | 1,412 | Rust | 中高 |
| 10 | storytold/deckcraft | +428 | 998 | Rust | 中高 |

⚠️ **已剔除的刷量农场**（全部创建于 2026-10-09 13:44–13:59 UTC，0 fork，随机词用户名，盗版 SEO topics）：KindStatesman/KMS-Pico、VarnishSerpentBurn/Discord-Quest-Completer、navyofficerpipe/Discord-Server-Raider、passrhymegazebo/AnyUnlock、Clawfitzfilter/Display-Fusion、powderdiverpillar/Total-Commander、hyperrobinclash/Better-Discord、CoralFireRadial/StartAll-Back、PatchTechnician/Ads-Blocker、photonrajditch/Windows-Optimizer。此类仓库通常以「破解版软件」为诱饵分发恶意代码，请勿下载。

---

## 三、群聊讨论精华

### 1. mhtsec/ARTEX（+972，总 2,333）

**场景分析员**：韩国银行黑客案的余波仍在发酵。作为 AI 自主渗透测试工具 ARTEX（原作 Autumn-27/ARTEX）的镜像，它已连续第二天占据增量榜首。

**质疑者**：异常信号在加重——fork 数已涨到 4,661，是 star 数（2,333）的两倍，这不是正常社区行为，更像有组织的 fork 农场在批量复制该仓库，可能用于洗白分发或规避下架。事件热度是真的，仓库本身的结构是假的。可信度：**中**。

**主编**：事件值得跟踪（韩国方面调查仍在进行），但再次强调：研究请看原作 Autumn-27/ARTEX，这个镜像的 star/fork 数据已失去参考意义。

### 2. storytold/wordcraft（+957，总 1,987，Rust）

**场景分析员**：本期真正的主角。WordCraft 是 ArtCraft 团队用纯 Rust 净室重写的 Microsoft Word：ribbon、样式、修订、邮件合并全套 Word 工作流，读写 .docx，188 页文档重排约 1.4ms，桌面端用 egui 原生渲染（非 Electron），还内置 389 个命令的 MCP 接口让 AI Agent 直接驱动。据 LinkedIn 披露，该团队的方法是**用 AI 反编译 Photoshop/Word 二进制后净室重写**——这是「AI 重写商业软件」方法论的第一个成建制案例。

**质疑者**：四天曲线 354→626→957 稳步爬坡，无单日脉冲；有真实官网（getartcraft.com）、Discord 社区、44 个仓库的组织号和 LinkedIn/Facebook/Instagram 多平台自然讨论，不像刷量。两个保留意见：fork/star 比约 30% 偏高；「净室」声称能否经住微软法务检验是未知数。可信度：**中高**。

**主编**：本期最值得关注——它回答了一个行业级问题：当 AI 能以十分之一成本重写任何桌面软件时，开源替代品的长尾冲击开始了。

### 3. LosaLosSantos/aurelio-finance（+855，总 1,556，Python）

**场景分析员**：自托管个人财务分析工具（FastAPI + React + AI 财务顾问），连续第三天增量加速：309→392→855，是本榜唯一连续三天加速的项目。

**质疑者**：三天持续加速通常意味着有持续的社区传播链（自托管和理财社区都在转发），曲线形态健康、非单日脉冲；但增速斜率略陡，不排除有集中的社区帖推送。可信度：**中高**。

**主编**：值得关注——在满榜 Rust 重写工具里，它是「AI + 个人数据主权」赛道跑出来的少数应用层产品。

### 4. openai/math（+683，总 13,164，Lean）

**场景分析员**：OpenAI 的 722 篇 AI 数学手稿仓库，发布第四天，增量从 5,004 衰减到 683，进入长尾期。

**质疑者**：标准发布脉冲衰减曲线，官方出品无刷量动机。可信度：**高**。

**主编**：热度期已过，转入观察社区复用阶段——如果 Lean 社区开始基于这批手稿产出新证明，那才是真正的新闻。

### 5. zhongerxin/iPhone-use（+623，总 1,949，Python）

**场景分析员**：中国开发者的项目，让 Codex 通过 USB 操作真实 iPhone：引导安装、App 自动化、实时屏幕与截图回退。这是 browser-use 模式向移动端的延伸——「*-use」家族（让 Agent 操作真实设备）又添一员。

**质疑者**：10-07 仅 +9，10-08 冲到 883，10-09 回落 623，是典型的「被社区发现后脉冲」形态；开发者实名、项目描述具体、有真实使用场景支撑。可信度：**高**。

**主编**：值得关注——移动端 Agent 操作是浏览器自动化之后的下一个无人区，它卡住了 iOS 这个最难的入口。

### 6. storytold/gridcraft（+563，总 1,245，Rust）

**场景分析员**：Craft 系列的 Excel 重写——净室、纯 Rust、原生跨平台 + WASM 浏览器版，同样带 MCP 接口。目标是让 AI Agent 能直接操作电子表格。

**质疑者**：与 wordcraft 同组织同节奏（239→435→563），共享同一波关注度；系列仓库互相引流是事实，但每个都是独立完整的产品而非空壳占位。可信度：**中高**。

**主编**：作为系列一员值得关注，但判断整个 Craft 系列的成色，盯 wordcraft 的真实 .docx 兼容性测试就够了。

### 7. noahdunnagan/fsearch（+513，总 1,218，Rust）

**场景分析员**：macOS 全盘文件搜索工具：模糊文件名、容错拼写、索引内容 grep，号称 800 万文件约 1ms。对标 Everything（Windows）在 macOS 上的空白。

**质疑者**：10-08 创建当天 +690、次日 +513，两天破千——增速惊人但曲线符合「被大号推荐」的形态；性能宣称（8M 文件 1ms）需要第三方验证，且与知名 Linux 工具 FSearch（cboxdoerfer/fsearch）同名，有蹭名嫌疑，但作者不同、平台不同，更像巧合或致敬。可信度：**中高**。

**主编**：值得关注——macOS 上 Everything 级搜索是真实痛点，但建议等性能宣称被复测后再下结论。

### 8. nullmoth/nvidia-macos-driver（+490，总 1,943，Rust）

**场景分析员**：让 NVIDIA RTX 显卡（GTX 16 至 RTX 50 系）在 macOS 15 Sequoia 上跑 Metal 3 加速的第三方驱动，走 NVIDIA 开源内核模块 + Mesa NVK Vulkan + 自研着色器翻译器路线，目标用户是 Intel Mac + eGPU 玩家和黑苹果社区。VideoCardz 已报道，Reddit 有 RTX 5060/5070 Ti/3090/3060 的成功案例。

**质疑者**：10 月 7 日发布以来 560→853→490，热度真实且有硬件媒体背书；但要泼冷水：需关闭 SIP/AMFI/安全启动，目前仅 RTX 5060 完整验证，无 CUDA（跑 AI 没戏），macOS 已全面转向 Apple Silicon，这是「黑苹果时代尾声的绝唱」式项目。可信度：**高**（热度与真实性），但实用性评级低。

**主编**：值得关注作为技术奇观——用 Mesa/NVK 给 macOS 嫁接 NVIDIA 驱动是教科书级的黑客工程；作为日常工具则受众极窄。

### 9. storytold/cadcraft（+478，总 1,412，Rust）

**场景分析员**：Craft 系列的 AutoCAD 重写，净室纯 Rust，把 CAD 制图也纳入同一套「Agent 可驱动」命令体系。

**质疑者**：系列第三个上榜，节奏与其他成员一致；CAD 的用户群比 Office 窄得多，却拿到比 gridcraft 更高的总 star，可能受益于「连 AutoCAD 都敢重写」的猎奇传播。可信度：**中高**。

**主编**：系列成员，关注价值同 wordcraft——它证明了这套方法论不只适用于文档类软件。

### 10. storytold/deckcraft（+428，总 998，Rust）

**场景分析员**：Craft 系列的 PowerPoint 重写，主题、版式、动画全套，兼容 .pptx，同样 MCP 可驱动。

**质疑者**：系列第四个，曲线（200→346→428）是标准的首发爬坡；同组织四仓同榜有互相引流成分，但均为实质产品。可信度：**中高**。

**主编**：系列成员，结论同上——Craft 系列今天实质占据榜单四席，这才是今天真正的「榜单事件」。

---

## 四、趋势洞察

1. **「AI 反编译 + 净室重写」成建制出现，桌面商业软件的开源平替潮启动。** ArtCraft 一个组织用同一套方法论（AI 辅助逆向 → 纯 Rust 重写 → 内置 MCP 让 Agent 可驱动）批量产出 Word/Excel/PowerPoint/AutoCAD/Photoshop 的替代品，今日四仓同榜。如果 .docx/.psd 兼容性经住检验，这将是开源桌面软件史上第一次「供给端」被 AI 根本性改变——重写软件的成本不再约束品类数量。法务风险（净室声称 vs 微软/Adobe）是最大变量。

2. **warez 投毒农场开始系统性操纵 GitHub 榜单。** 今日原始 TOP 20 中一半是 15 分钟内批量创建、同日各刷 400–600 star 的盗版诱饵仓库（KMS-Pico、Total-Commander、Better-Discord……），话题标签直接写「cracked-2026」。它们利用「破解软件搜索流量 + 批量刷 star 上 trending」的组合拳分发恶意代码，而 GitHub 的清理速度明显落后于创建速度。任何 trending 类榜单若不做过滤，都在客观上为投毒农场引流。

3. **「*-use」设备操作家族扩到移动端，Agent 的操作面继续下沉。** zhongerxin/iPhone-use 让 Codex 经 USB 驱动真实 iPhone，叠加此前的 browser-use 系和本周 Craft 系列的「Agent 原生软件」（每个按钮都是命令、内置 MCP），一个清晰的方向是：新软件从设计第一天就假设用户是 Agent 而非人类。

---

## 五、数据说明

- **来源**：本地 `data/github_history.json`（562 个被追踪仓库的逐日 star 增量）与 `data/snapshots/20261010/snapshot_1125.json`（GitHub API 描述/topics/创建时间/fork 数）；ARTEX 事件、nvidia-macos-driver、Craft 系列背景经公开报道（VideoCardz、LinkedIn、Reddit 等）交叉核实。
- **口径**：「昨日增量」= UTC 日期 2026-10-09 的当日新增 star 数。本期 142/562 个仓库有当日数据，覆盖度好于上期但仍不全。
- **刷量剔除**：识别出 10 个 warez 刷量农场仓库（判定依据：同日 15 分钟内批量创建、0 fork、随机词用户名、盗版 SEO topics、单日孤立脉冲 400–614 star），已从榜单剔除并逐一点名；无法保证识别所有刷量行为。mhtsec/ARTEX 因 fork/star 比严重异常（4,661 vs 2,333）降级为「中」可信度但保留在榜（其热度由真实新闻事件驱动）。
- **局限性**：star 增量反映关注度而非实际采用度；快照 API 对部分仓库未返回描述/语言（表中语言以最新快照为准）；fork 农场等新型操纵手段可能未被完全识别。
