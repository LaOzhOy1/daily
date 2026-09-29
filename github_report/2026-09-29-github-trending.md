# GitHub 趋势研究报告 · 2026-09-29

> 数据口径：UTC 逐日 star 增量，榜单日期 **2026-09-28（UTC）**；总 star 为 2026-09-29 08:25（CST）本地快照点。
> ⚠️ 本期数据质量提示：358 个被追踪仓库中仅 83 个有 09-28 当日数据，117 个仓库的数据停留在 09-19（9 天前），导致 4 个「回退仓库」占据 TOP 10 席位，请结合备注阅读。

## 一、开头摘要

本期真实增量冠军是 **dzhng/jevgrep**（+274，周末三天 243→660→274）：把 Jev 用作 coding agent 的「语义 grep」——用自然语言问「这段代码是干什么的」来检索相关文件，标志着 Jev 从模型话题变成 agent 基础设施动词。同样值得重点看的还有 **Niko1221/Strata**（+265）：让 125B 参数的 Qwen3.8-Flash-Next 在 8GB 显存的游戏 PC 上跑到 60-95 token/s，本地大模型推理工程的新极限；以及第二支开源的 P(doom) MV **mexicat/pdoom-video**（周日单日 +1212）。

## 二、TOP 10 总表（2026-09-28 UTC 增量）

| 排名 | 仓库 | 昨日增量 | 总 star | 语言 | 可信度 |
|---|---|---|---|---|---|
| 1 | jackwener/wx-cli-again | +285* | 694 | Rust | 中高（数据陈旧） |
| 2 | dzhng/jevgrep | +274 | 1,426 | TypeScript | 高 |
| 3 | Niko1221/Strata | +265 | 1,071 | C++ | 高 |
| 4 | mexicat/pdoom-video | +236 | 1,772 | TypeScript | 高 |
| 5 | yetone/magpie | +181 | 1,588 | Go | 高 |
| 6 | HyNetworks/OpenGFW | +175* | 231 | Go | 中（数据陈旧） |
| 7 | joeseesun/qiaomu-download | +174* | 241 | Python | 中高（数据陈旧） |
| 8 | yihui-dev/awesome-opus5-5-videos | +159 | 702 | — | 中 |
| 9 | Contrastive-LM/CLM | +121 | 2,279 | Python | 高 |
| 10 | huangbai-AI/post-production-skill | +102* | 208 | — | 中（数据陈旧） |

\* 这四个仓库缺失 09-28（及 09-20 之后全部）数据，回退使用 09-19 增量值——**已是 9 天前的旧数据，排名参考价值有限**。
备注：若剔除陈旧数据，快照 `github_daily_top` 给出的真实候选序为：jevgrep > Strata > pdoom-video > magpie > awesome-opus5-5-videos > CLM > The-Quant-Trading-Vault(+92) > blueprint-animation(+86) > onetake(+83) > PDoomVideo(+81)。laya 自 09-24 起增量记录为 0（采集缺口，仓库实际总 star 已超 2.3 万）。

## 三、逐仓库群聊讨论精华

### 1. jackwener/wx-cli-again（+285* · 总 694 · Rust）

**场景分析员**：微信本地数据 CLI 的 Rust 重写版，查询/解密/导出。gh api 显示总 star 实际已涨到 757、fork 1,717——即使采集断了，生态仍在缓慢增长。

**质疑者**：这是它连续第四期靠 09-19 旧数据占位榜首，严格说已不构成「昨日趋势」。fork/star 比 >2 的实用主义特征依旧。**可信度：中高**（对项目本身）；**数据时效性：差**。

**主编**：建议从下期起将回退超过 3 天的仓库移出主榜改列附录——占着第一名却讲不出新故事，对读者不公平。

### 2. dzhng/jevgrep（+274 · 总 1,426 · TypeScript）

**场景分析员**：给 coding agent 用的语义代码检索 CLI：「问这段代码是干什么的」代替 grep 关键词，用 Jev 做相关性判断，返回相关文件与源码上下文。兼容 Claude Code / Codex，接 Vercel AI Gateway。作者 dzhng 是 AI SDK 圈知名开发者。

**质疑者**：周末三天 243→660→274，周日冲高周一回落，是 HN/社区周末发酵的典型形态；topics 克制且精准（jev、code-search、context-retrieval），无堆砌。**可信度：高**。

**主编**：值得关注——Jev 热潮至今最「实用主义」的落点：不卖模型，卖的是让现有 agent 立刻变聪明的一个命令。

### 3. Niko1221/Strata（+265 · 总 1,071 · C++）

**场景分析员**：把 Qwen3.8-Flash-Next（125B MoE、激活 6B）塞进 8GB+ 显存的游戏 PC：MoE 专家在 GPU/RAM/SSD 间分片调度 + 推测解码，RTX 5070 上 60-95 token/s，一键安装（Windows/Linux），本地起 OpenAI/Anthropic 兼容 API 给 coding agent 用。基于 llama.cpp/ggml，MIT。

**质疑者**：曲线 17→19→187→349→265 稳步爬坡，README 工程细节（分档量化表、校准脚本、故障排查）扎实到不像营销项目；日文技术圈（Hatena）已有实测传播。唯一疑问是单机 125B 的实际可用性边界，但作者自己把限制写得很清楚。**可信度：高**。

**主编**：值得关注——「数据中心级模型上游戏 PC」的工程样本，本地推理的 MoE 分片路线开始产品化。

### 4. mexicat/pdoom-video（+236 · 总 1,772 · TypeScript）

**场景分析员**：第二支开源的《I'm Upping My P(doom)》MV——但与 JohnHeibel 的 p5.js 手绘风不同，这支是 three.js 工程化路线：逐词卡拉 OK 排版、确定性渲染（每帧是歌曲时间的纯函数）、Demucs 分轨 + CTC/Whisper 强制对齐、4K60 离线导出（M5 Pro 上 2.5 小时）。创意、分镜、引擎全部由 Opus 5.5 在 Claude Code 里完成。

**质疑者**：周日单日 +1212 后周一回落到 236，Reddit r/singularity 热帖 + 中文 X/Threads 大量转发，传播路径真实可查；与上周 PDoomVideo 撞题材纯属同一首歌的两个独立实现。**可信度：高**。

**主编**：值得关注——两支同源 MV 可以对照研究「同一模型、不同工程审美」：p5.js 手绘派 vs three.js 排版派，docs/TREATMENT.md 是现成的教材。

### 5. yetone/magpie（+181 · 总 1,588 · Go）

**场景分析员**：菜单栏 agent 模型路由器（Codex on DeepSeek、Claude Code on Kimi），连续六天日增 113-392，总 star 稳步爬到 1,588。

**质疑者**：全周无暴涨无断档，是本榜单最「匀速」的曲线，典型的工具口碑扩散。**可信度：高**。

**主编**：持续关注——它已经从「新品」毕业为「常备工具」，模型套利需求被验证为常态而非热点。

### 6. HyNetworks/OpenGFW（+175* · 总 231 · Go）

**场景分析员**：DIY 流量检测引擎，协议研究与教学场景。

**质疑者**：09-19 旧数据占位，现状不明。**可信度：中**（时效性差）。

**主编**：同 wx-cli-again，建议移入附录观察。

### 7. joeseesun/qiaomu-download（+174* · 总 241 · Python）

**场景分析员**：yt-dlp 的 Agent Skill 封装，多平台视频下载/提音/字幕。

**质疑者**：09-19 旧数据；gh api 显示总 star 已到 341，仍在缓慢增长。**可信度：中高**（时效性差）。

**主编**：同上，移入附录观察更合适。

### 8. yihui-dev/awesome-opus5-5-videos（+159 · 总 702 · Markdown）

**场景分析员**：收集 Opus 5.5 生成的病毒视频及背后 prompt 的 awesome 清单，每条附「在 Skillry 上看原版 vs 实时重制」。

**质疑者**：09-27 单日 +441 的尖峰 + 为自家产品 Skillry 导流的明确动机，是「内容策展+私域引流」的标准打法；比纯刷量体面，但商业意图需要读者知情。**可信度：中**。

**主编**：可以作为 Opus 5.5 创意案例库翻阅，但别把它当中立榜单——它是 Skillry 的内容获客渠道。

### 9. Contrastive-LM/CLM（+121 · 总 2,279 · Python）

**场景分析员**：斯坦福系 CLM-8B 决策模型，发布第六天仍日增三位数，总 star 2,279——学术项目里少见的续航力。

**质疑者**：762→385→338→361→121 的缓降曲线健康；10 月初 CLM-35B 多模态版预告是下一个观察点。**可信度：高**。

**主编**：持续关注——续航证明它不是发布会一日游，System One 赛道的学术锚点已立住。

### 10. huangbai-AI/post-production-skill（+102* · 总 208 · 无语言）

**场景分析员**：给 AI 视频后期用的 Seedance 2.5 Skill：生成电影级 VFX、创意转场、三维 UI、动态镜头的提示词。目标用户是中文 AI 视频创作者。

**质疑者**：09-19 旧数据占位；纯提示词合集类 Skill 门槛低、同质化重。**可信度：中**。

**主编**：轻度关注——AI 视频工作流「Skill 化」方向没错，但需要新版本数据确认活力。

## 四、趋势洞察

1. **「P(doom) MV」成为 AI 创意工程的对照实验场。** 同一首歌、同一个模型（Opus 5.5），两周内出现两支全开源、技术路线迥异的实现（p5.js 手绘 vs three.js 排版），加上 prompt 策展仓库跟进——AI 生成内容第一次有了可对照、可复现、可教学的「流派样本」，创意编码的教材时代开启。
2. **本地推理的「贫民窟奇迹」持续加码。** Strata 把 125B MoE 拆到 GPU+RAM+SSD 三级存储跑在游戏 PC 上，与上周 laya-mlx（Apple Silicon）形成两条硬件民主化路线：MoE 架构的「激活参数小」特性正在被推理工程吃干榨净。
3. **Jev 完成从「模型」到「动词」的转变。** jevgrep 的出现意味着 Jev 不再只是被讨论的对象，而是嵌进其他工具名字里的基础设施（grep 的语义版）。当一个技术成为命名后缀，生态就算真正立住了。

## 五、数据说明

- **来源**：本地 `data/github_history.json`；`data/snapshots/20260929/snapshot_0825.json`（GitHub API 正常）；元数据经 `gh api` 交叉核验；Strata、pdoom-video、CLM 等背景用 GitHub README、Reddit、X、Hatena 等公开信息补充。
- **口径**：「昨日增量」= UTC 2026-09-28 当日新增 star；总 star 为 2026-09-29 08:25（CST）快照点；标 \* 的四个仓库回退使用 09-19 值。
- **局限性**：① **本期最大问题**：117 个仓库数据停在 09-19、158 个停在 09-26，仅 83 个有 09-28 数据——4 个回退仓库占据 TOP 10 第 1/6/7/10 名，榜单头部失真，已在备注中给出剔除陈旧数据后的真实排序；② laya 等仓库 09-24 起增量记录为 0 与实际状态矛盾，属采集缺口；③ 历史 daily 值会被后续快照修订；④ 周末效应：09-28 为周日，开发者活跃度天然偏低，绝对增量普遍缩水；⑤ 可信度评级为主观判断。
