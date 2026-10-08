# GitHub 趋势周报 · 2026-10-01 ~ 2026-10-07

> 数据口径：UTC 逐日 star 增量的 7 日合计；总 star 为 2026-10-08 09:56（CST）本地快照点。
> 本期窗口内仅发布过一期日报（10-04），本周报基于原始增量数据 + 公开报道整理。

## 一、本周总览

本周 GitHub 被一个事件统治：**OpenAI 于 10 月 6 日把未发布的内部前沿模型产出的 722 篇数学手稿（372 个成果族）直接倒进公开仓库 `openai/math`**，两天狂揽 9,682 star——AI 数学发现跳过期刊、以 GitHub 为首发平台的时代正式到来。其余主线：「常驻 AI 同事」落地战（OpenAI Dots 发布 48 小时后 CopilotKit 开源 OpenDots 平替，本周 +2,770）、Meta 开源 Muse 硬件 SDK（+1,660）、以及 Agent Skill 作为内容分发格式在全球开发者中爆发（answer-me-with-html、huashu-art-motion、easyread、yomiyasu 等中日项目扎堆）。值得注意的是：连续两周霸榜的 Jev 生态本周全面退出头部，流量被 OpenAI Decisions API 和数学事件吸走。

## 二、本周 TOP 10（7 日增量合计）

| 排名 | 仓库 | 7日增量 | 总 star | 语言 | 一句话定位 |
|---|---|---|---|---|---|
| 1 | openai/math | +9,682 | 9,725 | Lean | OpenAI 未发布模型的 722 篇数学手稿 |
| 2 | CopilotKit/OpenDots | +2,770 | 2,791 | TypeScript | OpenAI Dots 的开源自托管平替 |
| 3 | QingYunA/answer-me-with-html | +2,070 | 2,077 | JavaScript | 让 Agent 用一页 HTML 回答复杂问题 |
| 4 | rehan-remade/universal-modder | +1,738 | 2,754 | Python | Claude Code 给任何 PC 游戏做 mod |
| 5 | alchaincyf/huashu-art-motion | +1,689 | 1,707 | JavaScript | 艺术动画 Skill：35 种风格让画动起来 |
| 6 | facebookincubator/muse-gadget-sdk | +1,660 | 1,660 | C | Meta Muse 的 ESP32/树莓派硬件 SDK |
| 7 | kargulstudio/sales-crm | +1,636 | 1,637 | TypeScript | Next.js 16 脚手架，规则全在 CONVENTIONS.md |
| 8 | KKKKhazix/AIHOT | +1,365 | 5,571 | TypeScript | 自找热点自写日报的网站框架 |
| 9 | Louis-CFM/coucou | +1,329 | 4,028 | Swift | Mac 刘海/iPhone 上的 agent 监工与审批 |
| 10 | CAPCOM-TD-OSS/REDox | +1,003 | 1,131 | C# | CAPCOM 下一代引擎 REX 的 .NET 数据引擎 |

榜外值得记录：mizorewww/x_gift_bot +942（X Premium 赠送工具，灰色地带）、sganggs/Stronghold-Protocol +922（明日方舟同人自走棋）、Jakeschincariol/replica-skill +877（11 个克隆任意应用的 Claude Skill）、nykooi1/vibe-wise +745（边 vibe coding 边教学）、rauchg/gdp-ts +740（Vercel CEO 的 TS 授权证明库）、Edwardxlai/easyread +692（本地论文翻译）、elstongun/leviathan +666（agent 大数据集记忆索引）、chasmlol/SkyCraft +648（Skyrim×Minecraft 缝合）。

## 三、本周三大主线

### 主线 1：openai/math —— AI 数学发现的「GitHub 首发」时代

10 月 6 日，OpenAI 将内部未发布前沿模型面向约 4,000 个研究级数学问题产出的成果公开：**722 篇手稿、372 个成果族，Apache-2.0，附 Lean 形式化证明与 10 篇推理摘要**；平均每个成果消耗约 3 小时 ChatGPT Pro 级思考算力，多数成果源自单 agent 单次提示。OpenAI 坦承未形式化的手稿可能存在问题，将随形式化进展持续修订并保留全部历史版本。[Unite.AI](https://www.unite.ai/openai-releases-722-math-manuscripts-from-an-unreleased-ai-model/ "citation"), [THE DECODER](https://the-decoder.com/openai-dumps-372-ai-generated-math-proofs-on-github-telling-the-academic-world-to-keep-up/ "citation")

**小组点评**：这是本周、也可能是本季度最重要的仓库事件。它把「AI 做数学」从发布会 PPT（8 月 Astra 的 10 个证明）变成了可 clone、可引用、可逐行核验的公共资产；同时留下两个悬而未决的问题——未形式化部分的正确率，以及「不发布模型只发布产物」的透明度争议。数学界的同行评审压力才刚刚开始。

### 主线 2：「常驻 AI 同事」落地战与硬件化

- **OpenDots**（+2,770）：OpenAI 9 月 29 日发布付费产品 Dots，48 小时后 CopilotKit 开源 MIT 平替——可自托管、可换任意 OpenAI 兼容模型、每个 Dot 配独立电脑（浏览器/文件/终端），支持文字/语音/Slack 三端同上下文。⚠️ 警惕榜外的 **feder-cr/dots**：实为刷量机器人项目 invisible_dots 改名蹭热点（自称「反检测机器人」，31,810 star 的老仓库），请勿混淆。[futurpulse](https://futurpulse.com/always-on-ai-coworkers-openai-dots-vs-copilotkit-opendots/ "citation")
- **muse-gadget-sdk**（+1,660）：Meta 开源 Muse 助手的 ESP32/树莓派 SDK（Apache-2.0），Nat Friedman 亲自官宣，配套 5,000 台官方 Home Link 免费送订阅用户。注意：Muse 跑在云端，设备只是终端，且条款保留随时收回 token 的权利。[Unite.AI](https://www.unite.ai/meta-open-sources-muse-gadget-sdks-for-diy-ai-hardware-devices/ "citation")
- **coucou**（+1,329）：Mac 刘海和 iPhone 锁屏上的「agent 监工」——盯着你的 Claude Code/Codex/Cursor，需要审批时从刘海或锁屏一键批准。多个 agent 并行时代的「人机接口」补件。

**小组点评**：三条线合起来是一幅完整图景——agent 正从「聊一次走一次」变成「常驻、有电脑、有身体、需要你审批」的同事。本周的产品形态创新密度（订阅制官方版、48 小时开源平替、硬件 SDK、刘海监工）超过了过去一个季度。

### 主线 3：Agent Skill 成为新的内容分发格式

本周榜单被「Skill 化」项目刷屏，且东亚开发者表现抢眼：

- **answer-me-with-html**（+2,070）：让 Agent 用一页排版精良的 HTML 回答复杂问题，而非一堵文字墙——「答案即网页」；
- **huashu-art-motion**（+1,689）：35 种艺术风格、9 种解说语法的艺术动画 Skill；
- **easyread**（+692）：本地 PDF 论文翻译成「舒服的中文」，原文对照 + 边读边问；
- **yomiyasu**（+723）：把 AI 生成的生硬日语推敲成自然日语的 Agent Skill；
- **replica-skill**（+877）：11 个免费 Claude Skill，逆向 → 重建 → 修 bug → 修用户痛点，克隆任意应用；
- **gdp-ts**（+740）：Vercel CEO Guillermo Rauch 亲自下场，把 Haskell 的「Ghosts of Departed Proofs」移植到 TypeScript——敏感函数必须持有编译期「授权证明」才能调用，让一整类越权 bug 无法通过类型检查；并附带教 agent 应用该模式的 Skill。[GitHub](https://github.com/rauchg/gdp-ts "citation")

**小组点评**：Skill 正在重演 2008 年 App Store 的剧情——它是一种低门槛、可组合、自带分发渠道（`npx skills add`）的内容格式。本周的爆发有两个新特征：**创作者从英文圈扩散到中日圈**，以及**大厂核心人物亲自写 Skill**（rauchg）作为工程理念的传播载体。gdp-ts 尤其值得单读：它可能是「agent 时代 API 安全设计」的第一个范式级答案。

## 四、本周每日节奏（数据侧）

- **10-01 ~ 10-03**：Dots 余温（OpenDots 连续三天 600-1000+）、Muse Gadgets 发布（10-02）、universal-modder 高位横盘；明日方舟同人 Stronghold-Protocol 与 SkyCraft 带动游戏 mod 线。
- **10-04**：sales-crm 单日 +1,046（作者 Marcel Kargul 的 X 帖子 52 万浏览带量）；本期唯一一期日报记录了 OpenDots 登顶。
- **10-05 ~ 10-07**：answer-me-with-html 与 huashu-art-motion 接棒 Skill 线；**10-06 openai/math 发布**，单日 +5,006，次日再 +4,676，吸走全站注意力，多数仓库 10-05 后增量明显回落。

## 五、趋势洞察

1. **GitHub 成为顶级科研成果的首发渠道。** openai/math 证明：当成果附带机器可验证的 Lean 证明时，「先发 GitHub、期刊评审后置」是成立的发布策略——这会倒逼学术界重写成果认定流程。
2. **「巨头闭源发布 → 48 小时开源平替」剧本固化。** Dots/OpenDots 是本月第二次（上月是 Jev/laya）。闭源产品的功能发布会自动触发开源社区的应答，先发窗口以天计。
3. **Jev 热退潮，决策模型进入「巨头化」阶段。** 连续两周霸榜的 Jev 生态本周无一进头部：OpenAI Decisions API（9-29 发布）把品类讨论从「社区复刻」拉回到「平台标配」，野生生态的流量红利期结束，接下来拼的是真实集成量。

## 六、数据说明

- **来源**：本地 `data/github_history.json`（UTC 逐日增量，7 日窗口 2026-10-01 ~ 10-07 合计）；`gh api` 实时元数据；公开报道（Unite.AI、THE DECODER、SegmentFault、X 等）。
- **口径**：「7 日增量」为窗口内各日增量之和；总 star 为 2026-10-08 09:56（CST）快照点；窗口内无数据的日期按 0 计。
- **局限性**：① 采集管道存在已知缺口（部分仓库多日无记录，如 coucou 10-04 后数据中断），7 日合计可能低估；② 历史 daily 值会被后续快照修订；③ star ≠ 采用度；④ openai/math 的 star 含大量「标记事件」性质的非技术受众；⑤ 本窗口仅一期日报，部分判断未经过三角色讨论流程。
