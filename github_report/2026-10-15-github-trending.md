# GitHub 趋势研究报告 · 2026-10-15

> 榜单数据日期：**2026-10-14（UTC）**，口径为逐日真实 star 增量（非当日 trending 榜）。本期 684 个被追踪仓库中仅 48 个有当日非零数据，覆盖度为近期最低，榜单代表性受限，详见文末数据说明。

---

## 一、开头摘要

今天最值得关注的是 **d2r-mobile**（+931）：把 Switch 版《暗黑破坏神 II：狱火重生》通过「静态指令重写 + Metal 图形层」原生跑上 iPhone/iPad/Mac，不模拟、不重写游戏逻辑，玩家已实机验证 60 fps——这是继 N64/PS2 静态重编译之后，「Switch 二进制直转 Apple 平台」新移植范式的第一个成熟样本。第二看点：**esp32-iphone-agent**（累计 2,221）用 7 美元的 ESP32 让 AI 通过 AirPlay「看」、USB HID「点」真实 iPhone，与软件路线的 iPhone-use 形成硬件对照组。另外，「重写一切桌面软件」赛道出现第二家成建制玩家（HeyPuter/everything），而榜单第三名 jackie-fmri-sim 疑似刷量占位，已标注低可信度。

---

## 二、TOP 10 总表

| 排名 | 仓库 | 昨日增量 | 总 star | 语言 | 可信度 |
|---:|---|---:|---:|---|:--:|
| 1 | jhaizhou-ops/d2r-mobile | +931 | 2,610 | C | 中高 |
| 2 | outcrawlai/scout | +675 | 760 | TypeScript | 中高 |
| 3 | StoopwenpueNq/jackie-fmri-sim | +469 | 469 | Python | 低 |
| 4 | storytold/figcraft | +456 | 1,112 | Rust | 中 |
| 5 | HeyPuter/everything | +397 | 838 | JavaScript | 中高 |
| 6 | deeplethe/solid-glass | +370 | 854 | TypeScript | 中高 |
| 7 | onehumanbeing/esp32-iphone-agent | +364 | 2,221 | C | 高 |
| 8 | Arekejoker/qwen21-nsfw-pose-skill | +298 | 1,619 | Python | 中 |
| 9 | storytold/craft-launcher | +276 | 2,732 | Rust | 中 |
| 10 | Caho1/open-claude-ui | +249 | 455 | TypeScript | 中高 |

---

## 三、群聊讨论精华

### 1. jhaizhou-ops/d2r-mobile（+931，总 2,610，C）

**场景分析员**：开源 iOS/macOS 兼容层，把你自己购买的 Switch 版《暗黑破坏神 II：狱火重生》（含术士君临资料片）原生跑在 iPhone/iPad/Mac 上。技术路线与模拟器完全不同：iPhone 和 Switch 同为 ARM，重写器只改动 Apple 内核拒绝的少数指令（线程指针寄存器、系统调用、定时器），其余字节原样执行；图形 API 在 Metal 上重新实现，着色器离线翻译。触屏操作全套重做，60 fps，「自带游戏文件」（BYOF）规避分发版权问题。Reddit r/diablo2 有实机讨论，文档详细到列出每个派生接口。

**质疑者**：三天曲线 865→482→931，非单日脉冲；文档中大量设备实测记录（A16 需 Legacy Device Pack、A13 以下不支持）是刷量农场写不出来的细节。两个保留项：fork 825/star 2,610 约 32% 偏高（游戏移植类项目玩家 fork 构建属常态，部分解释得通）；法律上是灰色地带，暴雪法务是长期变量。可信度：**中高**。

**主编**：本期最值得关注——它把「静态重编译」从复古主机（N64/PS2）推进到现役主机 Switch，且工程完成度罕见地高；这条路一旦走通，Android 移植只是时间问题。

### 2. outcrawlai/scout（+675，总 760，TypeScript）

**场景分析员**：Outcrawl 团队的开源浏览器 Agent，走 CDP（Chrome DevTools Protocol）路线做网页自动化，TypeScript 实现。定位与 browser-use 系同赛道：让 LLM 操作真实浏览器完成任务。

**质疑者**：10-13 创建、10-14 单日 +675 的孤立脉冲，fork 仅 25（3%）——典型的「发布日导流」形态，更像一次集中的社区发布（可能配合 Product Hunt 或帖子）而非刷量；但「Mirrored automatically from Outcrawl's own repository」这句描述暗示它是镜像仓，主仓热度被分流，单日数据参考价值打折。可信度：**中高**。

**主编**：可以一看——浏览器 Agent 赛道已挤（browser-use、Jev 系刚退潮），scout 能否活下来取决于 CDP 路线的稳定性是否真比竞品好，建议等一周看留存。

### 3. StoopwenpueNq/jackie-fmri-sim（+469，总 469，Python）

**场景分析员**：名义上是 fMRI（功能性磁共振）模拟器，但描述为空、无 topics、无文档，无法判断实际内容。

**质疑者**：红灯全亮：随机词用户名（与上周 warez 农场的命名模式一致）、创建当天即获全部 469 star、描述为空、无任何公开讨论或引用。这不是真实的学术工具传播形态，疑似占位/刷量仓库。可信度：**低**。

**主编**：不值得关注，建议采集侧将其加入刷量黑名单观察列表。

### 4. storytold/figcraft（+456，总 1,112，Rust）

**场景分析员**：ArtCraft 系列最新成员——Figma 式协作设计工具的净室 Rust 重写，补上了「设计」这一环，Craft 套件离全覆盖 Adobe+Office+Figma 又近一步。

**质疑者**：fork 497/star 1,112 = 45%，fork 农场污染仍在继续；系列进入「每出一个新仓就吃一波系列流量」的惯性期，单仓增量已不能反映独立价值。可信度：**中**。

**主编**：作为系列进展值得记录，但 Craft 系列的新闻价值正在从「技术震撼」转向「法务与兼容性验证」，后续只跟踪这两个硬指标。

### 5. HeyPuter/everything（+397，总 838，JavaScript）

**场景分析员**：Puter（知名「互联网操作系统」项目）团队入场「重写一切」：宣言式描述「从零重建并开源全世界的软件」，topics 直接列出 adobe/photoshop/office/cad。与 ArtCraft 的 Rust 路线不同，HeyPuter 用 JavaScript，目标是跑在浏览器里的软件宇宙。

**质疑者**：Puter 主仓有数万 star 的存量信誉，这不是碰瓷小号；10-13 创建后 391→397 连续两天稳定流入，形态健康。但「重建全世界的软件」这种宏大叙事营销浓度极高，目前仓库内容厚度待验证。可信度：**中高**。

**主编**：值得关注——「净室重写」从单个团队的行为变成了赛道竞争（Rust 派 vs JS 派），这才是本周最重要的结构变化。

### 6. deeplethe/solid-glass（+370，总 854，TypeScript）

**场景分析员**：面向 AI 应用的设计系统：Material 质感、物理动效，基于 shadcn/Tailwind，主打「Agent UI / chat UI」场景——给 AI 产品的聊天和 Agent 界面提供成套组件。

**质疑者**：232→98→370 的波浪形曲线略不寻常（隔日反弹），可能对应两次社区帖曝光；fork 仅 11，比例偏低，说明看的人多、用的人少，设计系统类项目的典型早期形态。可信度：**中高**。

**主编**：可以关注——「AI 应用长什么样」正在从各家自绘走向标准化设计系统，这是该方向最早卡位的项目之一。

### 7. onehumanbeing/esp32-iphone-agent（+364，总 2,221，C）

**场景分析员**：用一块 7 美元的 ESP32-S3 让 AI 操作真实 iPhone：AirPlay 投屏当「眼睛」，USB HID 模拟键鼠当「手」，接任意 OpenAI 兼容视觉模型。不需要 Mac、不需要开发者账号、不需要越狱——这是把 iPhone-use 的软件方案翻译成硬件黑客方案，成本压到一杯咖啡钱。

**质疑者**：922→805→364 是健康的发布后衰减；topics 精准（airplay/usb-hid/computer-use），技术原理清晰可验证（AirPlay 接收 + HID 注入都是成熟技术）。 fork 297 属正常偏高（硬件项目玩家 fork 适配）。可信度：**高**。

**主编**：持续关注——它和 iPhone-use 构成了移动 Agent 的软硬两条路线对照实验，ESP32 方案在成本和免越狱上明显占优，可能后来者居上。

### 8. Arekejoker/qwen21-nsfw-pose-skill（+298，总 1,619，Python）

**场景分析员**：Qwen-Image 2.1 的出图 Skill：作者级提示词配方 + NSFW LoRA + 136 种姿势的人偶控制，适配 Claude Code / Codex / Cursor 等主流 Agent。目标用户是 AI 绘图重度玩家。

**质疑者**：121→906→298 的脉冲衰减；NSFW 标签天然带来高 star 低讨论的传播形态，fork 347（21%）偏高但可解释（玩家 fork 存配方）。内容处于平台政策灰色地带，随时可能被限流或下架。可信度：**中**。

**主编**：不作推荐，但作为信号值得记录——「姿势控制 + 提示词配方」打包成 Skill 说明 AI 绘图的工程化程度在加深，合规版本的技术可以平移到正途。

### 9. storytold/craft-launcher（+276，总 2,732，Rust）

**场景分析员**：Craft 套件启动器，上周已讨论，本周增量回落（498→531→276）。

**质疑者**：fork 912/star 2,732 = 33%，污染持续；启动器本身无独立技术价值。可信度：**中**。

**主编**：不再单独评论，并入 Craft 系列整体观察。

### 10. Caho1/open-claude-ui（+249，总 455，TypeScript）

**场景分析员**：中国开发者作品：逆向拆解 Claude 官方桌面端 UI，纯手写 30 个 React 组件 + 8 项交互物理算法高保真还原，附带 3000+ 行逆向分析手册。定位是「学习样本 + 可复用组件库」，目标用户是前端工程师和想抄 Claude 交互细节的 AI 产品团队。

**质疑者**：10-14 创建当天 +249，fork 102（22%），对单日新项目属正常偏高；「逆向手册」的差异化定位清晰，无刷量特征。可信度：**中高**。

**主编**：值得关注——「逆向顶级产品 UI 并开源工程细节」是国内前端社区少见的硬核内容形态，3000 行手册的价值可能超过组件本身。

---

## 四、趋势洞察

1. **「静态重编译」移植范式从复古主机推进到现役 Switch。** d2r-mobile 证明 Switch 二进制可以只改几十条指令就在 Apple 平台原生执行（同 ARM 架构红利），这比模拟器效率高一个量级。如果 Android 版本被社区补完，「买一份 Switch 游戏全平台跑」将冲击主机厂商的移植生意，法务冲突几乎不可避免。

2. **「重写一切」从行为变成赛道。** HeyPuter/everything（JS/浏览器派）紧随 ArtCraft（Rust/原生派）入场，加上 figcraft 补齐设计工具，AI 辅助净室重写商业软件已经出现竞争格局。下一个观察点：谁的兼容性先通过真实文件考验，以及微软/Adobe/Figma 谁先动法务。

3. **移动 Agent 的硬件路线跑通。** esp32-iphone-agent 用 7 美元硬件 + AirPlay/HID 绕过苹果全部开发者门槛，与软件方案 iPhone-use 形成对照。当「让 AI 用手机」的成本降到一杯咖啡钱，移动自动化的玩家基数将指数级扩大，苹果的反应（封 HID？限 AirPlay？）值得跟踪。

---

## 五、数据说明

- **来源**：本地 `data/github_history.json`（684 个被追踪仓库）与 `data/snapshots/20261015/snapshot_1655.json`；d2r-mobile 技术细节经其官方文档与 Reddit 讨论交叉核实。
- **口径**：「昨日增量」= UTC 日期 2026-10-14 的当日新增 star 数；本期无回退数据（TOP 10 均有当日值）。
- **采集缺口**：仅 48/684 个仓库有 10-14 非零数据，为近期最低；榜单仅代表当日活跃子集，漏榜风险高。
- **局限性**：star 增量反映关注度而非采用度；fork 农场污染持续（storytold 系列 fork/star 比 33%–45%）；jackie-fmri-sim 疑似刷量占位已标注但保留原始排名以示数据原貌；d2r-mobile 处于版权灰色地带，关注其技术不代表认可传播侵权内容。
