# GitHub 趋势研究报告 · 2026-10-12

> 榜单数据日期：**2026-10-11（UTC）**，口径为逐日真实 star 增量（非当日 trending 榜）。本期 684 个被追踪仓库中仅 61 个有当日数据，覆盖度明显收窄，榜单代表性受限，详见文末数据说明。

---

## 一、开头摘要

今天的主角是 **wheresryan22/anatomy**（单日 +2,568）：一个 Claude Code Skill，能把一句技术概念变成一台可交互的等轴测「机器」——缓存穿透变成弹子锁、连接池变成龙门绘图仪，SVG+WebGL 手工级质感，已被 Nous Research 的 Hermes 收录为官方技能，是 Agent Skill 生态继 answer-me-with-html 之后又一个出圈爆款。另一个结构性现象：**storytold（ArtCraft）的 Rust 净室重写系列今天占据 TOP 10 中的六席**，但其 fork 数在两日内异常翻倍（wordcraft 594→1,715），热度真实性与 fork 农场嫌疑并存，需分开看。

---

## 二、TOP 10 总表

| 排名 | 仓库 | 昨日增量 | 总 star | 语言 | 可信度 |
|---:|---|---:|---:|---|:--:|
| 1 | wheresryan22/anatomy | +2,568 | 3,271 | JavaScript | 高 |
| 2 | storytold/wordcraft | +980 | 5,894 | Rust | 中高 |
| 3 | storytold/craft-launcher | +538 | 1,194 | Rust | 中 |
| 4 | t4t5/omdrop-owl | +381 | 2,094 | Shell | 中高 |
| 5 | storytold/gridcraft | +354 | 2,912 | Rust | 中高 |
| 6 | storytold/cadcraft | +276 | 2,651 | Rust | 中高 |
| 7 | zhongerxin/iPhone-use | +232 | 3,038 | Python | 高 |
| 8 | storytold/deckcraft | +206 | 2,026 | Rust | 中高 |
| 9 | npwitk/Macintosh-Skeletal-Filled | +204 | 389 | — | 中高 |
| 10 | storytold/soundcraft | +170 | 1,805 | Rust | 中 |

---

## 三、群聊讨论精华

### 1. wheresryan22/anatomy（+2,568，总 3,271，JavaScript）

**场景分析员**：一个 Claude Code Skill：你说「解释令牌桶限流」，它不让 AI 画方框箭头，而是**发明一台真实的机器**——弹子锁、龙门绘图仪、浓缩咖啡机——用几十个手工着色的零件搭成等轴测 SVG，配 WebGL 火焰/水流着色器，可拖拽可交互，数字读数由驱动零件运动的同一个模型产生。目标用户是写技术文档、博客、落地页的开发者。零依赖（纯 Node 内置模块），`npx skills add` 一键安装。

**质疑者**：10-08 创建、10-10 发布 1.0、10-11 单日 +2,568——标准爆款曲线。背书链完整：explainx 评测博客、ccleaks 报道、Nous Research 的 Hermes Agent 已将其移植为官方技能。fork/star 比正常（249/3,271），无刷量特征。唯一的「风险」是这类 Skill 的热度半衰期短。可信度：**高**。

**主编**：本期最值得关注——它展示了 Skill 的正确形态：把「工艺规则 + 工具箱 + 自验证流程」打包给 Agent，而不是又一个 prompt 集合。做技术内容的人都该试一次。

### 2. storytold/wordcraft（+980，总 5,894，Rust）

**场景分析员**：ArtCraft 的 Word 净室重写继续领跑系列，五天累计近 6,000 star，增量仍在爬升（354→626→957→980）。

**质疑者**：警报信号出现——fork 数从 10-10 的 594 暴涨到 1,715，两天翻了 1.9 倍，远超 star 增速；系列其他仓库同步出现 fork 翻倍（soundcraft 已达 1,013 fork / 1,805 star = 56%）。这与上周 ARTEX 镜像的 fork 农场模式相似，怀疑有第三方在批量 fork 该系列仓库（可能为 SEO、洗版或蹭流量矩阵号）。star 增长本身仍有社区讨论支撑，但数据已被污染。可信度：**中高**（对项目），**中**（对数据）。

**主编**：项目本身仍值得关注，但建议观察微软法务动向和真实 .docx 兼容性测评，别被 fork 数据误导。

### 3. storytold/craft-launcher（+538，总 1,194，Rust）

**场景分析员**：Craft 系列的应用启动器——把 Word/Excel/PPT/CAD/PS 等十几个重写应用统一成一个桌面入口，是 ArtCraft 从「单品」走向「套件」的标志。

**质疑者**：10-09 深夜创建，两天 1,194 star，全靠系列流量灌溉；启动器本身技术含量低，是借势产物。fork 420 同样偏高。可信度：**中**。

**主编**：作为「Craft 套件化」的信号值得关注，作为软件本身不值得单独关注。

### 4. t4t5/omdrop-owl（+381，总 2,094，Shell）

**场景分析员**：「非苹果设备的 AirDrop」——基于 OpenDrop 的跨平台隔空投送，topics 里的 omarchy 表明它蹭上了 DHH 的 Omarchy Linux 发行版热潮，目标用户是 Omarchy/Arch 玩家和苹果-安卓双机党。

**质疑者**：三天 2,094 star，增长平稳无脉冲；Shell 脚本项目的实现门槛低，但 AirDrop 协议的逆向实现（OpenDrop 一脉）有真实技术积累。蹭 Omarchy 热点是事实，但痛点真实。可信度：**中高**。

**主编**：值得关注——Omarchy 带动的 Linux 桌面文艺复兴正在产生自己的工具生态，这是其中的基础设施件。

### 5. storytold/gridcraft（+354，总 2,912，Rust）

**场景分析员**：系列中的 Excel 重写，净室纯 Rust，MCP 可驱动。

**质疑者**：与系列同节奏增长；fork 从 491 涨到 1,201，污染情况同 wordcraft。可信度：**中高**。

**主编**：系列成员，结论同 wordcraft——关注整个 Craft 现象即可，单仓库增量参考价值下降。

### 6. storytold/cadcraft（+276，总 2,651，Rust）

**场景分析员**：系列中的 AutoCAD 重写。

**质疑者**：fork 1,205，同样异常。CAD 用户群窄却 star 高于 gridcraft 之外的大多数成员，猎奇流量成分大。可信度：**中高**。

**主编**：同上，作为系列样本看待。

### 7. zhongerxin/iPhone-use（+232，总 3,038，Python）

**场景分析员**：让 Codex 经 USB 操作真实 iPhone，发布第六天仍有 +232，长尾比预期持久——说明「Agent 操作移动设备」的需求不是脉冲而是持续流入。

**质疑者**：曲线从 883→623→232 自然衰减，无异常；实名开发者，场景具体。可信度：**高**。

**主编**：持续关注——它是「*-use」家族里唯一保持日增 200+ 的，移动端 Agent 入口的价值在被反复确认。

### 8. storytold/deckcraft（+206，总 2,026，Rust）

**场景分析员**：系列中的 PowerPoint 重写。

**质疑者**：fork 1,034 / star 2,026，51% 的 fork 率是系列里污染最严重的之一。可信度：**中高**（对项目）/ 低（对 fork 数据）。

**主编**：系列成员，不单独展开。

### 9. npwitk/Macintosh-Skeletal-Filled（+204，总 389）

**场景分析员**：极客浪漫项目：逆向出苹果新 Mac 开机「hello」动画所用字体 Macintosh Skeleton 的 B-spline 控制点，让任何人能生成同款手写「hello」SVG 动画。目标用户是字体极客、前端动画玩家和苹果设计文化爱好者。

**质疑者**：10-10 创建、两天 389 star，fork 53 比例正常；纯情怀向项目无营销动机，传播靠设计社区自来水。可信度：**中高**。

**主编**：值得关注一周——它没有什么实用价值，但「把苹果未公开的字体资产逆向成开源格式」是复古计算文化的标志性事件。

### 10. storytold/soundcraft（+170，总 1,805，Rust）

**场景分析员**：系列中的 Pro Tools（专业音频工作站）重写——这是 Craft 系列里技术难度最高的品类之一。

**质疑者**：fork 1,013 / star 1,805 = 56%，全系列最高，数据污染最严重；音频软件重写涉及延迟、插件生态等硬问题，净室重写 Pro Tools 的可行性存疑。可信度：**中**。

**主编**：系列成员中成色最需要验证的一个——音频工作站不是 UI 重写能解决的，观望。

---

## 四、趋势洞察

1. **Agent Skill 进入「作品级」阶段。** anatomy 单日 +2,568 并被 Hermes 收录为官方技能，证明 Skill 已能承载真正的工艺含量（自验证、几何审计、双主题渲染），而不只是 prompt 包装。Skill 生态的竞争壁垒正在从「点子」转向「工程质量」。

2. **fork 农场成为新的数据污染手段。** 继上周 ARTEX 镜像（fork 2 倍于 star）之后，Craft 系列六仓 fork 两日内同步翻倍（soundcraft fork/star 达 56%），批量 fork 正在被用作 SEO/洗版/矩阵号养号的工具。只看 star 的榜单已不够，fork 异常必须纳入可信度评估。

3. **Omarchy 效应外溢。** omdrop-owl（AirDrop 平替）借 Omarchy 话题三天 2,000+ star，DHH 的 Linux 桌面运动正在催生自己的配套工具链——这是今年桌面 Linux 罕见的生态性增长信号。

---

## 五、数据说明

- **来源**：本地 `data/github_history.json`（684 个被追踪仓库）与 `data/snapshots/20261012/snapshot_0824.json`；anatomy、Macintosh-Skeletal-Filled 等背景经公开报道与 GitHub API 交叉核实。
- **口径**：「昨日增量」= UTC 日期 2026-10-11 的当日新增 star 数；本期无回退数据（TOP 10 均有当日值）。
- **采集缺口**：仅 61/684 个仓库有 10-11 数据（上期 142/562），覆盖度大幅收窄，本榜单仅代表活跃子集，可能遗漏未被追踪或数据断档的热门仓库。
- **局限性**：star 增量反映关注度而非采用度；本期发现 fork 农场污染（storytold 系列、前期 mhtsec/ARTEX），相关仓库的 fork/star 结构异常已在正文标注，但无法保证识别全部操纵行为；Macintosh-Skeletal-Filled 未进入快照 github 列表，其描述来自 GitHub API 实时查询。
