# Skill 地图 — 精准择时

一句话说明：这是 14 张能力卡的入口地图——先在能力总表里按意图定位卡，再看依赖关系决定补读哪一张，最后按加载顺序执行；完整规格见 [`bundle/verified.yaml`](./bundle/verified.yaml)。

## 能力总表

| capability_id | slug | 中文标题 | 重要度 | 去向 |
|---|---|---|---|---|
| `cap.wave-accurate-timing-skill.wave-degree-and-direction-skill` | `wave-degree-and-direction-skill` | 定级定方向 | critical | promoted → 独立 skill |
| `cap.wave-accurate-timing-skill.structure-condition-vs-end-signal-skill` | `structure-condition-vs-end-signal-skill` | 结构条件与结束信号 | critical | promoted → 独立 skill |
| `cap.wave-accurate-timing-skill.correction-pattern-dictionary-skill` | `correction-pattern-dictionary-skill` | 调整形态词典 | critical | promoted → 独立 skill |
| `cap.wave-accurate-timing-skill.countertrend-entry-and-trade-point-taxonomy-skill` | `countertrend-entry-and-trade-point-taxonomy-skill` | 逆势抓底与三类交易点 | critical | promoted → 独立 skill |
| `cap.wave-accurate-timing-skill.bull-bear-divide-and-relabeling-skill` | `bull-bear-divide-and-relabeling-skill` | 多空分界点与上移下移 | high | promoted → 独立 skill |
| `cap.wave-accurate-timing-skill.trend-following-entry-skill` | `trend-following-entry-skill` | 顺势点 | critical | promoted → 独立 skill |
| `cap.wave-accurate-timing-skill.stop-target-and-exit-skill` | `stop-target-and-exit-skill` | 止损·目标·出局 | critical | promoted → 独立 skill |
| `cap.wave-accurate-timing-skill.position-decides-strategy` | `position-decides-strategy` | 位置决定策略 | high | router → 路由入口 |
| `cap.wave-accurate-timing-skill.short-term-entry-patterns` | `short-term-entry-patterns` | 短线买点 | high | router → 路由入口 |
| `cap.wave-accurate-timing-skill.sector-stock-selection-skill` | `sector-stock-selection-skill` | 板块选股 | high | router → 路由入口 |
| `cap.wave-accurate-timing-skill.high-probability-resonance` | `high-probability-resonance` | 高胜率结构与共振 | critical | router → 路由入口 |
| `cap.wave-accurate-timing-skill.multi-timeframe-crosscheck` | `multi-timeframe-crosscheck` | 多周期复核 | high | router → 路由入口 |
| `cap.wave-accurate-timing-skill.ambiguity-handling` | `ambiguity-handling` | 多标注与不确定性 | high | router → 路由入口 |
| `cap.wave-accurate-timing-skill.forecast-methods` | `forecast-methods` | 走势预测法 | high | router → 路由入口 |

- **promoted → 独立 skill**（7 张）：在 pack 模式下各自是一个带 `SKILL.md` 的独立目录，可被 description 直接命中；在 single 模式下仍是入口内部的一张卡。
- **router → 路由入口**（7 张）：pack 模式下只存在于 `wave-accurate-timing-skill-router/references/capabilities/`，由路由表按意图加载。

## 依赖关系（also_read）

下表列出 `verified.yaml` 中每张卡声明的 `also_read`，即在主卡执行完之后建议补读的卡（方向按 yaml 记录，未做对称展开）：

| 主卡 | 建议补读（also_read） |
|---|---|
| `wave-degree-and-direction-skill` | `position-decides-strategy`、`structure-condition-vs-end-signal-skill`、`multi-timeframe-crosscheck` |
| `structure-condition-vs-end-signal-skill` | `wave-degree-and-direction-skill`、`countertrend-entry-and-trade-point-taxonomy-skill`、`stop-target-and-exit-skill` |
| `correction-pattern-dictionary-skill` | `structure-condition-vs-end-signal-skill`、`countertrend-entry-and-trade-point-taxonomy-skill`、`bull-bear-divide-and-relabeling-skill` |
| `countertrend-entry-and-trade-point-taxonomy-skill` | `structure-condition-vs-end-signal-skill`、`trend-following-entry-skill`、`stop-target-and-exit-skill` |
| `bull-bear-divide-and-relabeling-skill` | `correction-pattern-dictionary-skill`、`stop-target-and-exit-skill`、`position-decides-strategy` |
| `trend-following-entry-skill` | `countertrend-entry-and-trade-point-taxonomy-skill`、`structure-condition-vs-end-signal-skill`、`stop-target-and-exit-skill` |
| `stop-target-and-exit-skill` | `countertrend-entry-and-trade-point-taxonomy-skill`、`trend-following-entry-skill`、`bull-bear-divide-and-relabeling-skill` |
| `position-decides-strategy` | `wave-degree-and-direction-skill`、`forecast-methods`、`trend-following-entry-skill` |
| `short-term-entry-patterns` | `countertrend-entry-and-trade-point-taxonomy-skill`、`position-decides-strategy`、`structure-condition-vs-end-signal-skill` |
| `sector-stock-selection-skill` | `position-decides-strategy`、`high-probability-resonance`、`countertrend-entry-and-trade-point-taxonomy-skill` |
| `high-probability-resonance` | `countertrend-entry-and-trade-point-taxonomy-skill`、`trend-following-entry-skill`、`multi-timeframe-crosscheck` |
| `multi-timeframe-crosscheck` | `wave-degree-and-direction-skill`、`structure-condition-vs-end-signal-skill`、`high-probability-resonance` |
| `ambiguity-handling` | `wave-degree-and-direction-skill`、`correction-pattern-dictionary-skill`、`stop-target-and-exit-skill` |
| `forecast-methods` | `wave-degree-and-direction-skill`、`position-decides-strategy`、`structure-condition-vs-end-signal-skill` |

几条成环的强依赖，实际使用时按这个顺序读：

- **定级 → 结构 → 买卖点**：`wave-degree-and-direction-skill` → `structure-condition-vs-end-signal-skill` → `countertrend-entry-and-trade-point-taxonomy-skill`／`trend-following-entry-skill`（级别定不下来，后面两步都无处落脚）
- **形态与分界点**：`correction-pattern-dictionary-skill` → `bull-bear-divide-and-relabeling-skill`（先认出是剪刀 / 镰刀 / 双节棍，才知道有没有多空分界点）
- **入场之后必接风控**：`countertrend-entry-and-trade-point-taxonomy-skill`、`trend-following-entry-skill` 都指向 `stop-target-and-exit-skill`（没有止损与出局的买卖点不算可执行结论）
- **复核链**：`multi-timeframe-crosscheck` ⇄ `high-probability-resonance`（大级别看不清才下钻，下钻后回到大级别确认共振）

## 加载顺序

1. **先读入口 `SKILL.md`**：single 模式读 `single/wave-accurate-timing-skill/SKILL.md`，pack 模式读 `pack/wave-accurate-timing-skill-router/SKILL.md`。入口里有「触发与不触发」「核心原则」「能力路由表」「加载规则」「边界与判停」五段，概览类问题读到核心原则即可回答，不必加载能力卡。
2. **按路由表加载 1 张卡**：拿用户意图去匹配路由表的「用户意图」列，命中后只加载对应的那一张卡（`references/capabilities/<slug>.md`）。
3. **最多补读 1 张**：任务确实跨域时（例如既判断这段调整是否结束、又要给出止损与目标），按上表的 `also_read` 再加载 1 张，总数不超过 2 张。
4. **非能力类查询走索引**：书名/作者/章节/整书概览 → `references/overview.md`；术语 → `references/glossary.md`；决策规则速查 → `references/cheatsheet.md`；路由表未覆盖的意图 → `references/capability-index.md`。
5. **判停**：路由表与索引都无法命中的意图，明确告知超出本书范围；多周期数据不足无法定级、结构标注存在多解且无法比较幅度、浪起点不明导致关键点位无法确定时，只观察不参与，并如实说明缺哪几项数据。
