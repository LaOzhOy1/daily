# GitHub 趋势研究报告 · 2026-09-25

> 数据口径：UTC 逐日 star 增量，榜单日期 **2026-09-24（UTC）**；总 star 为 2026-09-25 08:25（CST）本地快照点。
> 本期快照 GitHub API 正常；榜单与快照 `github_daily_top` 候选榜完全一致。

## 一、开头摘要

今天最值得关注的是 **Contrastive-LM/CLM**（+389）：斯坦福 Hazy Research 系团队（Christopher Ré、Azalia Mirhoseini 署名的 Notion 论文）开源的 System One 决策模型 CLM-8B，号称延迟比 Jev 低 9 倍、做 verifier 可把 DeepSWE 推到 81.6%——学术正规军正式杀入 laya 开辟的赛道。其次是 **mikehasa/golive-skill**（+873，单日冠军）：一个让 Agent 把 vibe-coding 产品真正「上线」（托管/数据库/域名/支付全用自己的账号）的开源 Skill，补上了 agent 工作流的最后一公里。

## 二、TOP 10 总表（2026-09-24 UTC 增量）

| 排名 | 仓库 | 昨日增量 | 总 star | 语言 | 可信度 |
|---|---|---|---|---|---|
| 1 | mikehasa/golive-skill | +873 | 874 | TypeScript | 中高 |
| 2 | driceroland/Search | +428 | 1,243 | Swift | 高 |
| 3 | Contrastive-LM/CLM | +389 | 812 | Python | 高 |
| 4 | jev-chat/jev-chat-jarvis | +368 | 6,068 | Kotlin | 中高 |
| 5 | yetone/magpie | +299 | 616 | Go | 高 |
| 6 | jackwener/wx-cli-again | +285* | 694 | Rust | 中高 |
| 7 | HyNetworks/OpenGFW | +175* | 231 | Go | 中 |
| 8 | joeseesun/qiaomu-download | +174* | 241 | Python | 中高 |
| 9 | Cosmicchibattle/zeroclaw-ui | +172 | 201 | TypeScript | 低 |
| 10 | JohnHeibel/PDoomVideo | +169 | 695 | JavaScript | 中高 |

\* 这三个仓库缺失 09-24 数据，回退使用 09-19 增量值。
备注：昨日榜首 laya 本日增量记录为 0（仓库本身正常、总 star 已达 23,032，疑为采集缺口，详见数据说明）；前天的刷量机器人集群（CodexDesk 等）增量全部归零，疑似已被平台处置。

## 三、逐仓库群聊讨论精华

### 1. mikehasa/golive-skill（+873 · 总 874 · TypeScript）

**场景分析员**：解决「agent 帮我写完代码，然后呢？」的问题：一个开源 Agent Skill + 零依赖 Node CLI，带 Agent 走 detect → plan → approve → apply → verify 五步，把产品部署到你自己的 Vercel/Netlify/Cloudflare/Supabase/Neon/GoDaddy 账号上，包括域名、邮箱、支付。强调无自家账号、无后端、无遥测。

**质疑者**：09-23 创建次日 +873，单日爆发型；topics 一口气堆了 20 个关键词（agent-skill、claude-code、codex、vercel、supabase……），营销嗅觉明显。但「全部用用户自己的账号、无遥测」是反 SaaS 锁定的好设计，切中 agent 编程普及后的真实痛点。**可信度：中高**。

**主编**：值得关注——vibe-coding 的瓶颈正在从「写代码」转向「上线运维」，这是第一个系统化解决后者的 Skill。

### 2. driceroland/Search（+428 · 总 1,243 · Swift）

**场景分析员**：Office Commun 的 3MB 极简 macOS 浏览器，第二天再增 428，总 star 翻倍到 1,243。

**质疑者**：两天连续高增、曲线未衰减，X 上的设计圈传播仍在发酵；无 topics 的「裸奔」元数据反而说明没做 SEO。**可信度：高**（连续两天验证了非刷量）。

**主编**：值得关注——连续两日高增证明这不是一日热点，「反臃肿浏览器」正在复制 Arc 早期的口碑路径。

### 3. Contrastive-LM/CLM（+389 · 总 812 · Python）

**场景分析员**：斯坦福 Hazy Research 血统的 CLM-8B：冻结 Qwen3-8B 编码器 + 两个约 20M 参数的对比学习投影头（InfoNCE），给「状态×候选动作」打分而不生成文本。零样本打平 Jev 且延迟低 9 倍；微调后作 verifier 把 DeepSWE 推到 81.6%、Terminal-Bench 2.1 到 87.6%。Apache-2.0，权重已上 Hugging Face。

**质疑者**：无描述、无 topics 的朴素仓库，两天 182→389 稳步爬升，靠 MarkTechPost、explainx 等技术媒体报道驱动，非营销号刷量。需注意 SOTA 数字来自微调头而非零样本，且 8B 比 laya 的 421M 重一个量级——「9 倍快」是同任务对比而非同功耗。**可信度：高**。

**主编**：值得重点关注——这是 Jev 赛道第一次迎来学术正规军，laya 的「社区野生替代」叙事升级为「可复现的研究方向」，10 月初还有多模态 CLM-35B。

### 4. jev-chat/jev-chat-jarvis（+368 · 总 6,068 · Kotlin）

**场景分析员**：微信/QQ/飞书聊天副驾，第四天上榜，增量 2640→552→368 持续回落但总盘破 6,000。

**质疑者**：降温曲线符合「裂变红利耗尽、进入观望期」的判断；合规风险未解。**可信度：中高**。

**主编**：关注价值递减——除非微信官方表态或产品迭代出新功能，否则可以移出每日观察清单了。

### 5. yetone/magpie（+299 · 总 616 · Go）

**场景分析员**：知名开发者 yetone 新作：macOS 菜单栏里的「agent 模型路由器」——让 Codex 跑在 DeepSeek 上、Claude Code 跑在 Kimi 上，一处切换所有 agent 的底层模型。目标用户是想省 API 钱或绕开单一厂商锁定的重度 agent 用户。

**质疑者**：09-23 创建，两天 317→299 稳定输出，作者自带开源社区信誉（topics 克制、描述清晰），无刷量特征。**可信度：高**。

**主编**：值得关注——「模型套利」工具化是 agent 普及的必然产物，菜单栏形态把这件事做到了零摩擦。

### 6. jackwener/wx-cli-again（+285* · 总 694 · Rust）

**场景分析员**：微信本地数据 CLI 的 Rust 重写版，查询/解密/导出一条龙。

**质疑者**：连续第三天回退 09-19 数据，采集管道对它已失效，真实近况不明；fork（1,697）远高于 star 的实用主义特征仍在。**可信度：中高**（评级基于旧数据，置信度打折）。

**主编**：维持关注但降级为「周报级别」——数据采集恢复前无法判断新动向。

### 7. HyNetworks/OpenGFW（+175* · 总 231 · Go）

**场景分析员**：「DIY 版 GFW」——开源的流量检测/过滤引擎，让个人或小团队自建深度包检测设备。典型场景是网络协议研究、家庭网关实验、隐私教学演示。

**质疑者**：回退 09-19 数据；题材天然敏感，star 量小且增长平缓，无刷量迹象但也无社区背书信号。**可信度：中**。

**主编**：技术上值得关注（把 GFW 级能力变成可研究的开源组件），但使用场景需要读者自行判断合规性。

### 8. joeseesun/qiaomu-download（+174* · 总 241 · Python）

**场景分析员**：通用视频下载 Agent Skill：封装 yt-dlp，支持 YouTube/B 站/X/TikTok 等平台链接的下载、提音频、扒字幕；微信视频号转交专用姊妹项目，明确「绝不自动化操作微信客户端」。

**质疑者**：回退 09-19 数据；yt-dlp 套壳类工具门槛不高，但作为 Skill 形态接入 agent 工作流是新包装。作者 joeseesun 在中文独立开发圈有信誉积累。**可信度：中高**。

**主编**：轻度关注——「下载」是 agent skill 化的自然品类，它的价值在于合规边界画得比同行清楚。

### 9. Cosmicchibattle/zeroclaw-ui（+172 · 总 201 · TypeScript）

**场景分析员**：自称「Zeroclaw 的安装配置 UI」，面向想搭建 Zeroclaw 工作流的用户。

**质疑者**：09-24 当天创建即上榜；topics 是 15 个 zeroclaw-* 变体关键词的暴力堆砌（zeroclaw-alternative、zeroclaw-trading、zeroclawinstall……），教科书级 SEO 劫持手法，与前天刷量集群的命名风格（形容词+名词账号）同源。**可信度：低**。

**主编**：不值得关注——蹭热点品牌的寄生型仓库，建议不 clone 不运行，并警惕「zeroclaw」相关搜索结果被污染。

### 10. JohnHeibel/PDoomVideo（+169 · 总 695 · JavaScript）

**场景分析员**：现象级 AI 生成 MV《I'm Upping My P(doom)》的全部源码：Opus 5.5 在 Claude Code 里两代生成，自己写分镜（STORYBOARD.md）、自己给并行子 agent 写风格指南（ANIMATION_GUIDE.md），用 p5.js 逐帧作画再 ffmpeg 合成。YouTube 播放 12.9 万，Reddit r/singularity 热帖。

**质疑者**：典型的发布周热点衍生品，热度绑定 Opus 5.5 话题周期；但它是「作品开源」而非空洞 demo—— pipeline 可复现、素材齐全，作者还抽出了可复用的 ClaudeAnimationBase（同作者，+82）。**可信度：中高**。

**主编**：值得关注——这是「模型自编自导自画」工作流的第一个完整开源样本，ANIMATION_GUIDE.md 本身比视频更有研究价值。

## 四、趋势洞察

1. **System One 决策模型从「社区野生」升级为「学术赛道」。** laya（社区爆款）热度回落之际，斯坦福系的 CLM-8B 带着论文、基准和 Apache-2.0 权重进场——「小模型做判断、大模型做生成」的架构分工正在获得学术正统性，预计会有更多研究团队跟进，这个品类的竞争才刚开始。
2. **Agent 工具链向「写完代码之后」延伸。** golive-skill（部署上线）与 magpie（模型路由）同日上榜，说明 agent 工作流的痛点正从生成环节转向运营环节：上线、省钱、换模型。Skill 生态的「水电煤」层开始成型。
3. **AI 生成文化产品开始「开源化」。** PDoomVideo 把一支病毒传播 MV 的完整生产线（含模型自己写的分镜与风格指南）开源，标志着 AI 生成内容从「看结果」进入「学过程」阶段——这类仓库的教育价值可能超过娱乐价值。

## 五、数据说明

- **来源**：本地 `data/github_history.json`；`data/snapshots/20260925/snapshot_0825.json`（GitHub API 正常，含 `github_daily_top`）；元数据经 `gh api` 交叉核验；CLM、golive-skill、PDoomVideo 等背景用公开报道（MarkTechPost、explainx、Hugging Face 模型卡、GitHub README、Reddit）补充。
- **口径**：「昨日增量」= UTC 2026-09-24 当日新增 star；总 star 为 2026-09-25 08:25（CST）快照点；wx-cli-again、OpenGFW、qiaomu-download 回退使用 09-19 值（表中标 \*）。
- **局限性**：① laya 的 09-24 增量记录为 0 与其实际状态（总 star 23,032、当日仍有提交）矛盾，判断为采集缺口而非真实零增长，故未上榜，此为本期最大数据瑕疵；② 历史 daily 值会被后续快照修订（如 laya 的 09-23 值由 1,787 修订为 3,128），昨日报告数字以修订后为准；③ 回退数据仓库的真实热度可能被低估；④ 可信度评级为主观判断；⑤ star ≠ 采用度。
