# GitHub 趋势研究报告 · 2026-10-18

> 榜单数据日期：**2026-10-17（UTC）**，口径为逐日真实 star 增量（非当日 trending 榜）。本期原始 TOP 30 中混入至少 15 个 warez 刷量农场仓库（2026-10-17 19:10 UTC 的 90 秒内批量创建、各刷 ~200 star、0 fork），已全部剔除，正文按剔除后排名呈现。

---

## 一、开头摘要

今天最有趣的是一场「行为艺术」：XScreenSaver 作者 jwz 亲手创建 **xscreensaver-official/xscreensaver**，仓库内容只有一句话——「There is no official XScreenSaver GitHub repository」，用以对抗假冒仓库，Mastodon 社区集体转发求 star，一天冲上榜单。实质技术看点是 **net-merge**（+381，把所有网卡带宽聚合起来下载）和 **uncharted_pc**（《神秘海域》合集静态重编译原生跑上 Windows，接棒 d2r-mobile 的移植新浪潮）。另外，warez 刷量农场本期规模升级到 90 秒批量创建 15+ 仓，榜单过滤已成日常工作。

---

## 二、TOP 10 总表（已剔除刷量农场）

| 排名 | 仓库 | 昨日增量 | 总 star | 语言 | 可信度 |
|---:|---|---:|---:|---|:--:|
| 1 | rohit267/net-merge | +381 | 793 | Go | 中高 |
| 2 | aicodeking/leanrea | +356 | 398 | Python | 中 |
| 3 | anujasid/blender-ai-mcp-addon | +330 | 616 | Python | 中高 |
| 4 | Noniv/web-ocean | +183 | 489 | HTML | 中高 |
| 5 | Leonxlnx/earshot | +180 | 680 | Python | 中高 |
| 6 | deeplethe/solid-glass | +137 | 1,706 | TypeScript | 中高 |
| 7 | HeyPuter/everything | +130 | 2,052 | JavaScript | 中高 |
| 8 | xscreensaver-official/xscreensaver | +115 | 705 | — | 高 |
| 9 | Supermedo/uncharted_pc | +89 | 1,257 | C++ | 中高 |
| 10 | ahwootech/BRUTAL | +84 | 1,790 | C# | 中高 |

⚠️ **已剔除的刷量农场**（全部创建于 2026-10-17 19:10 UTC 前后 90 秒内，0 fork，「pre-activated installer」话术，盗版 SEO topics，各刷约 200 star，另有约 15 个各刷 40–110 star）：DAEMON-Pro、Data-Grip、Directory-Opus、Display-Fusion、DVD-Creator、Discord-Server-Cloner、Discord-Quest-Completer、FabFilter-Pro/Total、FL-Studio、Filmora-15、Easy-Worship、Glary-Utilities-Pro、GrayKet、Designcenter-NX、Claude-Jailbreak-Prompt、Cinebench 等。这是继 10-09、10-14 之后该农场第三次大规模出动，且出现 undress.ai 等违规内容诱饵，请勿访问下载。

榜外值得关注：chenglou/handwired（+42，总 1,676，「把普通 JavaScript 代码变成神经网络」，React 核心团队前成员 Cheng Lou 新作）、MyLuxy/overdrive（+61，PS5 自制软件商店）。

---

## 三、群聊讨论精华

### 1. rohit267/net-merge（+381，总 793，Go）

**场景分析员**：把 Windows/Linux/Mac 上所有网络接口同时用起来：Wi-Fi + 有线 + 手机 USB 共享网络做逐连接负载均衡（TUN + Wintun 实现），下载器多线程吃满全部带宽。目标用户是带宽饥渴的下载党、网络条件复杂的远程办公者。

**质疑者**：10-12 创建，五天累计 793 star，本期 +381 是峰值但非孤立单日脉冲；fork 30（4%）比例健康，topics 精准无 SEO 垃圾。功能类工具靠社区帖导流的正常形态。可信度：**中高**。

**主编**：值得关注——「聚合所有网卡」是每个多网络环境用户都想过但很少有人做成的需求，Go+TUN 的实现路线轻量靠谱。

### 2. aicodeking/leanrea（+356，总 398，Python）

**场景分析员**：一个 8KB 的 Agent Skill，号称替代 REA（Reverse Engineer Anything）逆向分析流程：不用 MCP，纯 CLI 工具组合，自称基准测试快 38%、便宜 35%。踩的是「MCP 太重，Skill 够用」的轻量化思潮。

**质疑者**：创建当天（10-17）即获全部 398 star 中的 356，单日脉冲形态；「8KB 替代 XX + 基准数字」是近期 Skill 营销的标准话术模板，基准测试无第三方复现。但 fork 79（20%）说明有人真在用。可信度：**中**。

**主编**：谨慎关注——它代表的「反 MCP 臃肿、Skill 极简主义」方向是对的，但这份具体的基准宣称需要等社区复测。

### 3. anujasid/blender-ai-mcp-addon（+330，总 616，Python）

**场景分析员**：Blender 的 AI 助手 + MCP 服务器：可视化对话、场景工具、多 Agent 工作流，兼容 OpenAI/Claude/Gemini 多家模型。让 Agent 直接操作 3D 创作软件——继文档、表格之后，Agent 的操作面扩展到 3D。

**质疑者**：10-15 创建，两天 616 star，fork 119（19%）比例正常；Blender MCP 此前已有知名开源实现（blender-mcp），这是差异化跟进者，热度可能借前作势能。可信度：**中高**。

**主编**：值得关注——3D 创作是 Agent 操作面最后几个空白领域之一，多模型兼容策略比单绑 Claude 的前作更讨巧。

### 4. Noniv/web-ocean（+183，总 489，HTML）

**场景分析员**：从零手写的实时 WebGPU 海洋渲染器：FFT 波浪、白沫、太阳闪光、物理天空与云、自由相机，全部装进一个 61KB 的 HTML 文件，Chrome 打开即看。描述坦诚标注「Built with Claude Code (Opus 5.5)」——这是 vibe coding 作品的标准展示形态。

**质疑者**：10-16 创建，两天 489 star，单日 +183 为主力；fork 83（17%）正常。纯演示项目无持续价值，但作为「AI 辅助图形学作品」样本真实可信。可信度：**中高**。

**主编**：值得点开看一次——61KB 单文件装下一片物理正确的海洋，是「AI 结对编程能做出什么」的最佳演示品之一。

### 5. Leonxlnx/earshot（+180，总 680，Python）

**场景分析员**：「编码 Agent 的耳朵」：让 AI 能听声音、评审音频、生成音效，CPU 即可运行，MCP 接口对接 Claude Code。目标用户是做游戏/视频/播客的独立开发者——Agent 写代码之余还能管音频。

**质疑者**：10-15 创建，三天 680 star，曲线平稳；fork 39（6%）健康。音频 MCP 是真实空白点，非蹭热点。可信度：**中高**。

**主编**：值得关注——Agent 的感官扩展（视觉之后是听觉）正在逐一补齐，CPU-only 的设计降低了接入门槛。

### 6. deeplethe/solid-glass（+137，总 1,706，TypeScript）

**场景分析员**：AI 应用设计系统，上周已上榜（当时 +370），本周增量回落至 +137，累计 1,706 star，进入平稳增长期。

**质疑者**：从脉冲转入长尾，曲线形态转为健康；fork 21 仍偏低，说明观望者多使用者少。可信度：**中高**。

**主编**：持续观察——它能否从「被围观的 demo」变成「被采用的设计系统」，未来两周的 fork 转化率是关键指标。

### 7. HeyPuter/everything（+130，总 2,052，JavaScript）

**场景分析员**：Puter 团队的「重写全世界软件」计划，上周上榜后增量稳定在 130 上下，累计破 2,000 star。

**质疑者**：397→397→130→130 的台阶式回落，热度回归理性；fork 294（14%）正常。项目实质内容进展仍需验证。可信度：**中高**。

**主编**：持续关注但不急——等它放出第一个能打开真实 .docx/.psd 的应用再升级评价。

### 8. xscreensaver-official/xscreensaver（+115，总 705）

**场景分析员**：本期最妙的存在。jwz（Jamie Zawinski，Netscape 早期功臣、XScreenSaver 作者）创建的仓库，全部内容只有一句「There is no official XScreenSaver GitHub repository」——因为假冒的 XScreenSaver GitHub 仓库太多，他干脆注册「official」名号放置一个「官方否认声明」。Mastodon 上 jwz 亲自发帖（"Dear Lazyweb, Due to dumbasses…"），社区大 V 转发号召「给这个仓库点 star」，用 star 数把这个声明顶到搜索结果前面。

**质疑者**：这不是项目热度而是社区治理行为的副产品；但 star 增长完全真实（集体行动的自发结果），且指向的公益目的明确——压制假冒仓库。可信度：**高**。

**主编**：值得记录进本期报告——「用一个空仓库对抗假冒」是开源社区自卫的创造性案例，也提醒所有人：GitHub 搜到的「official」仓库不一定是官方的。

### 9. Supermedo/uncharted_pc（+89，总 1,257，C++）

**场景分析员**：《神秘海域：德雷克合集》静态重编译，原生跑在 Windows 上。与上周 d2r-mobile（Switch→iPhone）同属「重编译移植」浪潮，方向相反：从主机向 PC 搬。

**质疑者**：10-15 创建，三天 1,257 star，fork 68（5%）健康；静态重编译 PS3 游戏的技术可行性已被 N64 重编译工具链验证，可信。法律上同样是 BYOF 灰色地带。可信度：**中高**。

**主编**：值得关注——d2r-mobile 和 uncharted_pc 一周内相继出现，「静态重编译移植」已从孤立事件变成连续浪潮，索尼/暴雪的法务反应是下一个看点。

### 10. ahwootech/BRUTAL（+84，总 1,790，C#）

**场景分析员**：免费开源的 C# 游戏框架：直访原生 API 和 Vulkan，可用来写游戏或自己的引擎。目标用户是想脱离 Unity/Godot 生态、追求极简依赖的 C# 开发者。

**质疑者**：10-14 创建，四天 1,790 star，增长平稳；fork 94（5%）健康。「又一个游戏框架」的生存率历来很低，但 Unity 收费风波后市场确实留了缝。可信度：**中高**。

**主编**：可以关注——C# 游戏开发者在 Unity 信任危机后一直在找退路，BRUTAL 是最新的承接者，能不能活下来看三个月后的 commit 频率。

---

## 四、趋势洞察

1. **warez 刷量农场升级为「工业化出动」。** 本期农场在 90 秒内批量创建 15+ 仓库（上一波是 15 分钟 10 个），全部卡在 ~200 star 的同一量级——明显有脚本控制「刷到刚好上 trending」的阈值。更危险的是出现了 Claude-Jailbreak-Prompt、undress.ai 这类违规内容诱饵，农场的目标已从广告引流扩展到恶意分发。每日榜单的「农场过滤」已是必备工序。

2. **静态重编译移植成为连续浪潮。** d2r-mobile（Switch→Apple）之后，uncharted_pc（PS3→Windows）接棒上榜。AI 辅助逆向大幅降低了重编译的人力门槛，「主机游戏原生跑遍全平台」正在从极客实验变成流水线，主机厂商的独占壁垒面临结构性侵蚀。

3. **Agent 的「器官」继续增生，同时出现反 MCP 轻量化思潮。** earshot（听觉）、blender-ai-mcp（3D 操作）扩展 Agent 的操作面，而 leanrea「8KB Skill 替代 MCP 方案」的走红说明社区开始反思 MCP 协议的重量——Skill 生态的技术路线之争开始了。

---

## 五、数据说明

- **来源**：本地 `data/github_history.json`（937 个被追踪仓库）与 `data/snapshots/20261018/snapshot_0825.json`；xscreensaver 事件经 jwz 的 Mastodon 原帖及社区转发核实，web-ocean/net-merge 等经 GitHub API 实时查询补充。
- **口径**：「昨日增量」= UTC 日期 2026-10-17 的当日新增 star 数；本期无回退数据。
- **采集缺口**：937 个仓库中 108 个有当日非零数据，覆盖度约 12%，榜单仅代表活跃子集。
- **刷量剔除**：识别并剔除 30+ 个 warez 农场仓库（判定依据：2026-10-17 19:10 UTC 前后 90 秒内批量创建、0 fork、随机词用户名、「pre-activated installer」话术、star 聚集在 40–200 的脚本化量级）；已剔除仓库不代表全部操纵行为均被发现。
- **局限性**：star 增量反映关注度而非实际采用度；xscreensaver-official 的 star 属社区治理行动副产品，不代表软件采用。
