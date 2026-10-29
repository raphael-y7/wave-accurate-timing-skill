<h1 align="center">精准择时 Skill</h1>

<p align="center">中文 | <a href="README.en.md">English</a></p>

一套可直接使用的 AI skill 工具包——把陈晓东《精准择时——波浪理论实战策略》里的波浪内部结构择时方法，蒸馏成 14 张可单独触发、也可组合调用的能力卡。

它不是原书摘要，也不是读后感，而是把书中可复用的方法论拆成可触发、可执行、可测试的 skill 模块。

## 这套 skills 能解决什么问题

- 不先定级就谈买卖点：这段走势处在哪一级、往哪个方向走、该看哪个周期，先定下来，否则后面的止损、目标、仓位全是错的
- 把「调整走完」当「反转确认」：`{a}{b}{c}` 三浪齐了只算「具备结构条件」，它还能继续演变成剪刀式、镰刀式、双节棍式乃至浪中浪，并把高一级的结束点一起往下拖——重仓抄底被套大多出在这一步
- 这个低点能不能抄、它属于逆势点 / 转势点 / 顺势点里的哪一类、首仓下多重、继续跌下去还要不要补
- 止损放哪、目标定在哪、什么时候主动走、什么时候被动走、止损怎么逐级上移
- 多空分界点在哪、破了与没破分别怎么应对、标号该不该上移或下移
- 两种数法都说得通、日线看不出方向、多个买点同时出现时，到底怎么下单、下多重

## 蒸馏了什么

14 张能力卡，按「先定级定方向、再判结构是否结束、最后落到买卖点与出局」的顺序组织：

- **定级与结构判定**（3 张）：`wave-degree-and-direction-skill`（定级定方向）、`structure-condition-vs-end-signal-skill`（结构条件与结束信号）、`correction-pattern-dictionary-skill`（调整形态词典：剪刀 / 镰刀 / 双节棍与四种特殊结构）
- **交易点定位**（4 张）：`countertrend-entry-and-trade-point-taxonomy-skill`（逆势抓底与三类交易点）、`bull-bear-divide-and-relabeling-skill`（多空分界点与上移下移）、`trend-following-entry-skill`（顺势点）、`short-term-entry-patterns`（短线买点）
- **风控与出局**（1 张）：`stop-target-and-exit-skill`（止损·目标·出局）
- **位置、共振与复核**（4 张）：`position-decides-strategy`（位置决定策略）、`high-probability-resonance`（高胜率结构与一点三级共振）、`multi-timeframe-crosscheck`（多周期复核）、`ambiguity-handling`（多标注与不确定性）
- **选股与预测**（2 张）：`sector-stock-selection-skill`（板块启动时选股）、`forecast-methods`（走势预测法）

## 两种打包模式：single 与 pack

同一套 14 张能力卡，按两种粒度各编译了一次。两者内容完全相同，区别只在「agent 能看到几个入口」。

| | single（单一入口） | pack（compact pack，多入口） |
|---|---|---|
| 可发现入口 | **1 个**：`wave-accurate-timing-skill` | **8 个**：1 个来源路由入口 + 7 个已晋级独立 skill |
| 14 张能力卡放在哪 | 全部在入口的 `references/capabilities/` 里，由入口按路由表按需加载 1 张（跨域最多 2 张） | 7 张高频卡各自独立成 skill；其余 7 张仍在 router 的 `references/` 里 |
| 触发方式 | 只有入口的 description 参与匹配，进入后靠路由表分流 | 7 个高频能力可被 description 直接命中，少一跳 |
| 升级维护 | 替换 1 个目录 | 替换 8 个目录 |

pack 里被晋级为独立 skill 的 7 张卡：

- `wave-degree-and-direction-skill` — 定级定方向
- `structure-condition-vs-end-signal-skill` — 结构条件与结束信号
- `correction-pattern-dictionary-skill` — 调整形态词典
- `countertrend-entry-and-trade-point-taxonomy-skill` — 逆势抓底与三类交易点
- `bull-bear-divide-and-relabeling-skill` — 多空分界点与上移下移
- `trend-following-entry-skill` — 顺势点
- `stop-target-and-exit-skill` — 止损·目标·出局

### 该装哪一种

按你的工作方式选，**只装一种**：

| 你的工作方式 | 推荐 | 原因 |
|---|---|---|
| 用 DSH / Codex / Claude Code 等有 skills 目录，希望列表干净 | single | 只占 1 个入口，能力一张不少 |
| 日常问题高度集中在「现在什么级别 / 这个低点能不能抄 / 止损目标 / 调整是什么形态 / 多空分界点 / 顺势买点」 | pack | 这 7 类正是被晋级的独立 skill，能直接命中 |
| 要分发给多个 agent 或团队，各自按需取用 | pack | 可以只装其中几个独立 skill，不必整包 |
| 只想装一次、不想维护多个目录 | single | 升级时只替换 1 个目录 |

> 两版由同一个 Bundle 编译，能力内容一致。**同时安装会重复触发**，请只装一种。

## 效果示例

### 示例 1：调整走成「剪刀式二次分解」，这个低点能不能抄

**用户问题**

"这段调整走成剪刀式二次分解了，`{c}` 再下移在 15.40，现在能不能抄底？止损放哪？"

**skill 如何判断**

- `structure-condition-vs-end-signal-skill`：先分清「具备结构条件」与「结束信号」——`{a}{b}{c}` 三浪齐了只说明「可以结束了」，仍可继续演变；要看到次一级三浪反转、并**验证收在关键低点/高点之外**，才算结束信号
- `countertrend-entry-and-trade-point-taxonomy-skill`：只有条件具备、没有结束信号时，当前点只能归入「逆势点」；而逆势点的前置条件是大周期方向明确，方向不明只能观察
- `stop-target-and-exit-skill`：止损放本浪起点之外，也就是 `{c}` 低点 15.40 以下；分批建仓、每批止损各管各的

**最终回答示例**

> 先说结论：这个点只能算「逆势点」，不能当「底」。
>
> 第一层，`{a}{b}{c}` 三浪走齐只是「具备结构条件」。书里的定义是「可以结束了」，不是「已经结束」——它还能继续演变成镰刀式、双节棍式甚至浪中浪，并把结束点一路往下拖。要变成可以反向建仓的「转势点」，得同时看到次一级三浪反转和验证收在关键高点之外，少一个都不算。
>
> 第二层，就算分类成逆势点，也有前置条件：大周期方向必须先定下来。你只给了日线这段调整，没说周线往哪走——按规则，大周期方向不明时只能观察，不能建仓。
>
> 第三层，止损没有第二种算法：放 `{c}` 低点 15.40 之外。不能因为「跌得够多了」就把止损挪近。首仓多大取决于你的风险偏好：书里只要求「分批」，**没有给统一比例**，能力卡里的建议上限是首仓 1/3，`{b}` 下移 / `{c}` 再下移 再补，每批止损独立。
>
> 两个照实说的边界：一是「验证收住」书里没给量化容差（收在关键点以上多少算收住），得你自己约定并写进预案；二是 A 股 T+1 下「当日跌破 15.40」当天走不掉，一字跌停还会直接穿越止损位。

### 示例 2：顺势回调，能不能买、止损和目标填什么

**用户问题**

"周线 C 上破 A 高点 21.30 了，日线回调 `{a4}` 15.80、`{b4}` 18.20、`{c4}` 16.35 没破 `{a4}`，60 分线（a）上破（b）下移高点 17.40、回抽收在 16.90 以上。现在能买吗？止损放哪、目标多少？"

**skill 如何判断**

- `trend-following-entry-skill`：顺势点有三个必要条件——高一级趋势已确立（周线 C 上破 A 高点 21.30）、本级别调整出现结束信号（60 分（a）上破（b）下移高点 17.40 并验证收在 16.90 以上）、回调低点未破前一个关键低点（16.35 高于 15.80）；三条对上才判为顺势点
- `stop-target-and-exit-skill`：止损放**本浪起点之外**，这笔交易依托的是 60 分线这波调整，止损就在 60 分调整浪低点以下；目标设在高一级浪「具备结构条件」处，不是固定百分比；主动出局与被动出局事先分设；止损只上移不下移
- 输入契约缺项先问：60 分调整浪低点没给、周线内部结构没给，这两格不猜

**最终回答示例**

> 定性上这是顺势点，不是抄底：周线 C 上破 A 高点 21.30 已经把高一级趋势定下来，日线回调 15.80 → 18.20 → 16.35 没破 `{a4}`，60 分（a）上破（b）下移高点 17.40 后又验证收在 16.90 以上，三个必要条件都对上了。
>
> 但止损这一格我现在填不了。规则是「放本浪起点之外」，这笔交易依托的是 60 分线这波调整，止损得放在 60 分调整浪低点以下，而你给的最低点只有日线的 15.80。硬拿 15.80 当止损，等于用高一级的低点止损，能力卡明确说这样风险不可控。所以先补一个数：60 分这波调整的最低点是多少。
>
> 目标同样不能现在编：它是「高一级浪具备结构条件处」，需要周线这一段的内部结构，你没给，先空着。
>
> 补完这两个数，还要把三件事事先写下来：主动出局（涨到目标结构就走）、被动出局（出现反转信号就走）、止损迁移（行情往上走，止损只上移不下移）。另外「可接受止损空间」在书里是定性判断、**没有给数值标准**，得按你自己的风险偏好定，写进预案。

## 这些 skill 是怎么生成出来的

这套 skill 使用 **[cangjie-skill](https://github.com/kangarooking/cangjie-skill)** 的 RIA-TV++ 流水线生成，整个流程分六个阶段：

1. **整书理解（Adler 分析）**——用 Mortimer Adler 的分析阅读法，对全书做结构、解释、批判、应用四步拆解
2. **并行提取**——同时派多个专项提取器（框架、原则、案例、反例、术语），从原文中提取候选方法论单元
3. **三重验证筛选**——每个候选必须通过三项检验：书内至少有 2 处独立佐证（跨域）、能回答书中未明说的新问题（预测力）、不是常识（独特性）
4. **RIA++ 构造**——按 R（原文引用）/ I（用自己的话重写）/ A1（书中案例）/ A2（未来触发场景）/ E（可执行步骤）/ B（边界与盲点）六个维度结构化
5. **Zettelkasten 链接**——找出能力卡之间的依赖、对比、组合关系，生成能力索引与路由表
6. **触发与输出测试**——为每张卡设计触发盲测题（含诱饵题：该触发时要触发，不该触发时要沉默）与输出评测场景，未通过的卡回炉重做，回炉后再做回归验证

这本书的蒸馏难点在于「作者主张」与「证据强度」必须分开标注：全书图证都是事后标注的既成走势，没有一个含亏损单的完整账户复盘；「验证收住」这类关键判据原书没有给量化容差。所以每张卡都带边界与盲点段，把「书里说了什么」和「这条有多可信、哪里会失效」分开写。

## 测试与验证

本仓库连生成过程的测试材料一起发布：入口目录下的 `test-prompts.json` 是固定用例集（`single/wave-accurate-timing-skill/` 与 `pack/wave-accurate-timing-skill-router/` 各一份），`test-results.md`（仓库根目录）是逐项判卷与复核轮补测记录——包含方法、分项判定、未单测的挂账项，不是只留一句「全部通过」。

- **盲测方法**：独立盲测代理（未参与蒸馏）只拿到技能路径与用户请求，先判「会不会触发、加载哪张卡」，再实际执行完整分析并写入文件；同时提供相邻技能（《精准数浪》《波浪理论》《道氏理论》）供混淆判断
- **用例集条数**：入口级 `test-prompts.json` 共 9 条 = 3 条正例 + 3 条诱饵 + 3 条边界；另有 2 个真实任务输出用例（T7 / T8）
- **触发判定**（照 `test-results.md` 原文）：正例 3 / 3 正确触发并正确执行；诱饵 3 / 3 未触发（其中 2 条正确转出到相邻技能）；边界 2 / 2 判定合理，第 3 条（T+1 可执行性）当批未单独实测，记为待补测
- **输出判定**：T8 与能力卡 E 段步骤逐条对应；T7 因场景本身缺 60 分调整浪低点，止损按规则判停、不猜价位——记的是「卡住的地方」而不是「通过了」
- **复核轮补测**（2026-10-24）：edge-03 补测通过；T7 补上 60 分低点后复算，止损 16.88、目标 18.20（假设已注明）、风险回报比约 1.5:1；双 skill 近邻负例 4 / 4 单选无双重触发；触发套件复测 8 / 9，唯一分歧是「单纯数浪」在未装《精准数浪》的环境下由本技能接住；R 段引文逐字核对 38 / 38
- **遗留与口径**：记录为无遗留；本仓库没有调平计数、没有改写判卷结果，也没有据此推算任何通过率

## 仓库结构

```text
wave-accurate-timing-skill/
├── README.md              ← 你正在看的
├── README.en.md           ← English version
├── LICENSE                ← MIT
├── BOOK_OVERVIEW.md       ← 阶段 0 产出：全书 Adler 分析
├── DIGEST.md              ← 阶段 5 产出：面向读者的整书精华长文
├── INDEX.md               ← 阶段 3 产出：skill 总览 + 依赖关系
├── verified.md            ← 通过三重验证的 14 个单元
├── coverage-audit.md      ← 阶段 1.5 产出：原书任务覆盖审计
├── needs-review.md        ← 阶段 1.5 产出：待核查事项与缺口
├── TEST_SUMMARY.md        ← 阶段 4 产出：压力测试摘要
├── CANGJIE_ADAPTATION.md  ← 仓颉适配说明
├── GITHUB_REPO.md         ← 仓库元数据
├── test-results.md        ← 测试结果记录
├── candidates/            ← 阶段 1 产出：原始候选池
│   ├── frameworks.md      ← 框架与方法候选
│   ├── principles.md      ← 原则 / 规则 / 计算候选
│   ├── cases.md           ← 书中案例候选
│   ├── counter-examples.md← 反例与边界候选
│   └── glossary.md        ← 术语候选
├── rejected/              ← 阶段 1.5 产出：被淘汰的单元 + 原因
├── bundle/                ← 编译事实源
│   ├── verified.yaml      ← 能力元数据、判据与去向
│   ├── cards/             ← 能力卡源文件（六段结构）
│   └── book/              ← overview.md + glossary.md
├── single/                ← single 模式（1 个入口 + 全部能力卡）
│   └── wave-accurate-timing-skill/SKILL.md  ← 入口：触发 + 路由表 + 加载规则（同目录含 test-prompts.json）
└── pack/                  ← pack 模式（1 个路由入口 + 7 个晋级 skill）
    └── */SKILL.md         ← 8 个 skill；router 目录附带 test-prompts.json
```

## 如何使用

先把仓库克隆下来：

```bash
git clone https://github.com/raphael-y7/wave-accurate-timing-skill.git
```

### 装 single（推荐先试这个）

```bash
# macOS / Linux
cp -r wave-accurate-timing-skill/single/wave-accurate-timing-skill ~/.agents/skills/
```

```powershell
# Windows
Copy-Item -Recurse .\wave-accurate-timing-skill\single\wave-accurate-timing-skill "$env:USERPROFILE\.agents\skills\"
```

### 装 pack

只复制含 `SKILL.md` 的目录，不要把 `pack/` 下的两个 json 一起拷进 skills 目录：

```bash
# macOS / Linux
cd wave-accurate-timing-skill/pack
cp -r wave-accurate-timing-skill-router \
      wave-degree-and-direction-skill \
      structure-condition-vs-end-signal-skill \
      correction-pattern-dictionary-skill \
      countertrend-entry-and-trade-point-taxonomy-skill \
      bull-bear-divide-and-relabeling-skill \
      trend-following-entry-skill \
      stop-target-and-exit-skill ~/.agents/skills/
```

```powershell
# Windows
$pack = ".\wave-accurate-timing-skill\pack"
$dest = "$env:USERPROFILE\.agents\skills"
@('wave-accurate-timing-skill-router','wave-degree-and-direction-skill','structure-condition-vs-end-signal-skill','correction-pattern-dictionary-skill','countertrend-entry-and-trade-point-taxonomy-skill','bull-bear-divide-and-relabeling-skill','trend-following-entry-skill','stop-target-and-exit-skill') |
  ForEach-Object { Copy-Item -Recurse -LiteralPath (Join-Path $pack $_) -Destination $dest }
```

> `~/.agents/skills` 是 DSH 的 skill 目录；用别的 agent 时换成它自己的 skills 目录即可（例如 Claude Code 是 `~/.claude/skills`）。

### 怎么确认装好了

装完问一句"这段调整的 `{c}` 再下移在 15.40，能不能抄底、止损放哪"，看 agent 是否先分「具备结构条件 / 结束信号」、再判「逆势点」并给出 15.40 以下的止损，而不是直接告诉你"可以分批建仓"。装的是 single 时，它会先读入口再按路由表进能力卡；装的是 pack 时，`structure-condition-vs-end-signal-skill` 与 `stop-target-and-exit-skill` 会被 description 直接命中。

## 来源

- 《精准择时——波浪理论实战策略》陈晓东 著
- 全书蒸馏，共产出 14 张能力卡

## 声明

本仓库只发布蒸馏后的 skill、索引与规则速查材料，不包含原书 PDF、EPUB、OCR 文件、截图或全书转写稿。能力卡中出现的原文引用仅用于标注方法论出处和保持可审计性。

书中所有判据（「验证收住」的容差、分批比例、可接受止损空间、共振条件、板块启动条件等）都是案例与经验归纳，原书未提供统计回测背书，多处阈值原书根本没有给出，使用时需按标的自行测试并声明所用口径。本仓库内容不构成投资建议。

## License

[MIT](./LICENSE)
