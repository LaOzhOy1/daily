# GitHub 趋势研究报告 · 2026-10-19

> 榜单数据日期：**2026-10-18（UTC）**，口径为逐日真实 star 增量（非当日 trending 榜）。本期原始榜单再次混入两波刷量农场（90 秒批量创建的 warez 家族约 15 仓、各刷 97 star；游戏外挂主题家族 3 仓、各刷 106 star），已全部剔除，正文按剔除后排名呈现。

---

## 一、开头摘要

今天的头条属于「静态重编译」浪潮第三棒：**MacNativeGames**（+246）让你用自己的《塞尔达传说：王国之泪》XCI/NSP 文件生成 Apple silicon 原生 Mac 应用——不模拟、ARM64 代码直接执行，X 和 Reddit 已刷屏，继暗黑2（d2r-mobile）、神秘海域（uncharted_pc）之后，主机游戏原生移植一周三连。另一条重磅是大厂动作：**腾讯混元开源 Hy-Memory 2.0**（+116），模型（30B-A3B，记忆基准超 Opus5）+ 框架 + MemHub 应用三层全开源，打通 10 种 AI 编程工具共享同一份本地记忆——「Agent 记忆」正式成为大厂争夺的基础设施层。

---

## 二、TOP 10 总表（已剔除刷量农场）

| 排名 | 仓库 | 昨日增量 | 总 star | 语言 | 可信度 |
|---:|---|---:|---:|---|:--:|
| 1 | Gathin23/tv-vibehack | +576 | 1,951 | Java | 中高 |
| 2 | ly05010419/MacNativeGames | +246 | 757 | C | 中高 |
| 3 | xiaoyang111222/cn-math-taxonomy | +223 | 329 | JavaScript | 中高 |
| 4 | feder-cr/git-ai | +193 | 2,297 | Go | 中高 |
| 5 | LiCinCan/blender-ai-mcp-addon | +191 | 786 | Python | 中 |
| 6 | alchaincyf/huashu-motion | +156 | 292 | JavaScript | 高 |
| 7 | aicodeking/leanrea | +138 | 641 | Python | 中 |
| 8 | deeplethe/solid-glass | +137 | 2,005 | TypeScript | 中高 |
| 9 | OpenMOSS/MOSS-Image | +121 | 689 | Python | 高 |
| 10 | Tencent-Hunyuan/Hy-Memory | +116 | 780 | Python | 高 |

⚠️ **已剔除的刷量农场**：① warez 家族（IOBIT-Driver-Booster、SystemCare-Pro、Microsoft-Visio、Adobe-Audition、Melodyne-5、KMS-Pico、Clion、Windows-Optimizer、ExitLag、AnyUnlock、Autodesk-CFD、IDM、HitFilm、Adobe-Substance-3d、Canva-Pro 等约 15 仓，全部同日创建、各刷 97 star、0 fork）；② 游戏外挂家族（fps-optimizer-rust、Fortnite-FPS-Booster、Minecraft-Aimbot，用户名均为「人名+随机后缀」模式，各刷 106 star，疑似外挂木马分发）。请勿下载此类仓库的任何文件。

榜外值得关注：Ansub/tv-detox（+104，tv-vibehack 的同概念轻量跟进）、interplains/zero-breach（+102，Candiru 间谍软件本地 IOC 扫描器，只读无依赖，安全应急价值高）。

---

## 三、群聊讨论精华

### 1. Gathin23/tv-vibehack（+576，总 1,951，Java）

**场景分析员**：「你的电视，去掉广告」——通过 ADB 给任意 Android TV 去臃肿应用，换装 tvOS 风格的干净桌面。描述里骄傲地写着「Built in an afternoon with Claude Code」：一下午 vibe coding 的产物。目标用户是被小米/国产电视开机广告折磨的普通用户。

**质疑者**：10-17 创建，两天 1,951 star，首日即爆款。fork 234（12%）健康；痛点极真实（电视广告人人喊打），「一个下午做完」的叙事本身也是传播点。可信度：**中高**。

**主编**：值得关注——它是「vibe coding 解决大众痛点」的样板：不需要是框架级创新，把一件人人想要的小事做到一键完成就够了。

### 2. ly05010419/MacNativeGames（+246，总 757，C）

**场景分析员**：用你自己的《塞尔达传说：王国之泪》XCI/NSP 游戏文件 + prod.keys，生成 Apple silicon 原生 macOS 应用——无模拟器，ARM64 代码直接跑，Reddit r/macgaming 实测「秒加载」。这是静态重编译浪潮的第三棒（d2r-mobile 的 Switch→iPhone、uncharted_pc 的 PS3→Windows 之后，Switch→Mac）。

**质疑者**：创建仅一天多即 757 star，X 上多语言疯传（英西中日），热度完全真实；fork 107（14%）正常。法律上仍是 BYOF 灰色地带，且塞尔达是任天堂法务部最敏感的品牌，下架风险全场最高。可信度：**中高**（对热度与技术），低（对存活期）。

**主编**：值得关注但抓紧看——任天堂的 DMCA 历来比暴雪和索尼都快，这个仓库的存活时间本身将是新闻。

### 3. xiaoyang111222/cn-math-taxonomy（+223，总 329，JavaScript）

**场景分析员**：初中数学知识图谱：课标映射 + 自适应诊断工具 + 1,407 道题库。目标用户是 K12 教育开发者、家教工具作者，以及想给孩子做自适应练习的家长开发者。

**质疑者**：10-18 创建，首日 +223 占总量 68%，典型「社区帖导流」单日脉冲；fork 82（25%）偏高，说明用的人多（教育类内容 fork 改题库的动机强）。可信度：**中高**。

**主编**：小众但扎实——知识图谱+题库这种「内容型开源」不靠技术炫技靠内容厚度，1,407 道题是真功夫。

### 4. feder-cr/git-ai（+193，总 2,297，Go）

**场景分析员**：「为 AI Agent 设计的 Git」——重新思考版本控制：当提交者主要是 Agent 而非人类，commit 语义、分支策略、审查流程该怎么变。topics 里的 scion 暗示与 SCION 网络架构团队的关联。目标用户是重度使用编码 Agent 的团队。

**质疑者**：10-15 创建，四天 2,297 star，增长平稳无异常脉冲；fork 257（11%）健康。概念先行，实现成熟度待验证，但「Agent-native 的 Git」是真问题。可信度：**中高**。

**主编**：值得关注——当 Agent 写了 80% 的代码，git blame 该指向谁？这个仓库在回答下一个五年的版本控制问题。

### 5. LiCinCan/blender-ai-mcp-addon（+191，总 786，Python）

**场景分析员**：Blender 的 AI 助手 + MCP 服务器（多模型兼容），上期以 anujasid/blender-ai-mcp-addon 上榜，本期作者名变为 LiCinCan——仓库创建时间不变，属账号转移或改名后的同一项目。

**质疑者**：fork 从 119 跳到 377（一天翻三倍），增速超过 star，与近期 fork 农场的污染模式吻合；所有权变更叠加 fork 异常，需要留意。项目本身多模型兼容的定位仍然成立。可信度：**中**。

**主编**：项目可继续关注，但其 fork 数据已不可信；建议以 issues/PR 质量而非 fork 数判断社区活跃度。

### 6. alchaincyf/huashu-motion（+156，总 292，JavaScript）

**场景分析员**：「话说」团队新作：让 Agent 一键直出商业级产品宣传片——会作曲、能指着某一帧画面让 Agent 改（GSAP 动效栈）。此前 huashu-art-motion 已多次上榜，这是从「艺术动画」到「商业视频」的升级。

**质疑者**：10-18 创建首日 +156，占总量 53%，团队惯用的发布日社区联动形态；作者在 Skill 生态有持续运营记录，fork 33（11%）正常。可信度：**高**。

**主编**：值得关注——国产 Skill 团队正在从「单点工具」走向「内容生产线」，宣传片生成是离钱最近的场景。

### 7. aicodeking/leanrea（+138，总 641，Python）

**场景分析员**：上期上榜的「8KB Skill 替代 REA」项目，本期增量 +138，两天累计 641 star，热度延续。

**质疑者**：首日 356 + 次日 138 的衰减形态正常；fork 111（17%）尚可。但「基准快 38%」的宣称至今仍无第三方复现。可信度：**中**。

**主编**：维持上期判断——方向对（Skill 极简主义），证据不足，等独立复测。

### 8. deeplethe/solid-glass（+137，总 2,005，TypeScript）

**场景分析员**：AI 应用设计系统，连续第三期上榜，累计突破 2,000 star，增量稳定在 130+。

**质疑者**：370→137→137 已完全脱离脉冲期进入稳态；fork 21 依旧偏低，「看多用少」的局面未改。可信度：**中高**。

**主编**：持续观察——star 稳增但 fork 不涨，说明它还没跨过「从展品到工具」的临界点。

### 9. OpenMOSS/MOSS-Image（+121，总 689，Python）

**场景分析员**：复旦 OpenMOSS 团队的官方图像生成模型：5B 参数 DiT 基座，主打高质量文字渲染、版面生成和高效微调——解决的是 AI 出图「字写不对」的老大难。

**质疑者**：10-16 创建，三天 689 star，学术团队官方发布，无刷量动机；fork 31（4.5%）正常。文字渲染是图像模型的硬指标，宣称需等社区实测。可信度：**高**。

**主编**：值得关注——国产开源图像模型又添一家正规军，文字渲染若属实，对海报/PPT 类生成场景是直接利好。

### 10. Tencent-Hunyuan/Hy-Memory（+116，总 780，Python）

**场景分析员**：腾讯混元 10 月 15-16 日发布的 Agent 记忆基础设施，三层全开源：专用模型 Hy-Memory-30B-A3B（约 3B 激活，记忆基准 55.49 超 Opus5 的 54.62）、记忆 SDK（聊天/工作/代码三类记忆管线）、MemHub 本地应用（打通 Cursor、Codex、Claude Code 等 10 种工具共享同一份记忆）。已在腾讯自选股、iWiki 等业务落地（多跳召回率 50%→90%）。

**质疑者**：官方发布 + 权威媒体（IT之家、凤凰网）报道链完整，热度真实；但「超 Opus5」是官方自报成绩（固定 20% 子样本），领先不足 1 分，第三方复现前应存疑；fork 66（8.5%）对大厂项目偏保守。可信度：**高**（对事件真实性），中（对基准宣称）。

**主编**：本期战略价值最高——记忆层开始争夺「跨工具工作流入口」，谁的 MemHub 成为你的默认记忆，谁就掌握了所有 Agent 的上下文；大厂亲自下场说明这块地被认为是基础设施。

---

## 四、趋势洞察

1. **静态重编译一周三连，正在改写主机游戏的分发格局。** d2r-mobile（Switch→iPhone）、uncharted_pc（PS3→Windows）、MacNativeGames（Switch→Mac）七天内相继上榜，AI 辅助逆向把移植成本压到个人开发者可承受。任天堂/索尼/暴雪的法务响应速度将决定这场浪潮是变成「模拟器 2.0」还是被扼杀在摇篮。

2. **Agent 记忆成为大厂下场的基础设施赛道。** 腾讯 Hy-Memory 三层全开源并用 MemHub 抢占「跨工具记忆入口」，信号明确：当用户在 Cursor/Codex/Claude Code 之间切换，谁的记忆层在底下托着，谁就有平台级话语权。预期 Mem0、MemOS 及字节/阿里会很快跟进。

3. **「一个下午 + Claude Code」成为新的发行话术。** tv-vibehack（去电视广告）两天近 2,000 star，作者把「一下午做完」写进描述当卖点——vibe coding 的叙事已从技术圈猎奇变成大众痛点的解决方案营销方式。

---

## 五、数据说明

- **来源**：本地 `data/github_history.json`（993 个被追踪仓库）与 `data/snapshots/20261019/snapshot_0824.json`；MacNativeGames 经 Reddit/X 讨论核实，Hy-Memory 2.0 经腾讯混元官网及 IT之家等报道核实。
- **口径**：「昨日增量」= UTC 日期 2026-10-18 的当日新增 star 数；本期无回退数据。
- **采集缺口**：993 个仓库中仅 53 个有当日非零数据（约 5%），覆盖度继续走低，榜单仅代表活跃子集。
- **刷量剔除**：识别并剔除两波农场——warez 家族（约 15 仓，各 97 star，90 秒批量创建）与游戏外挂家族（3 仓，各 106 star，人名+随机后缀用户名）；blender-ai-mcp-addon 的 fork 一日翻三倍疑受 fork 农场污染，已降级标注。
- **局限性**：star 增量反映关注度而非采用度；MacNativeGames、d2r-mobile 等移植项目处版权灰色地带，关注其技术不等于认可侵权使用；Hy-Memory 基准成绩为官方自报，尚待第三方复现。
