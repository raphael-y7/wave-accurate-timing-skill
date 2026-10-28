---
name: wave-accurate-timing-skill
description: |
  陈晓东《精准择时》体系入口（择时与买卖点）：定级定方向、结构条件与结束信号、调整形态词典、 逆势抓底与三类交易点、多空分界点、位置策略、顺势点、止损目标出局、短线买点、板块选股、 高胜率共振、多周期复核、多标注应对、走势预测。与同作者《精准数浪》技能区分：数浪入口解决 「浪怎么数、级别怎么标」，本入口解决「数完之后何时买、买多少、何时走」。不适用于纯基本面与消息面。
metadata:
  cangjie.generated-by: cangjie-tools v2.5.0
  cangjie.variant: router
  cangjie.bundle-id: bundle.wave-accurate-timing-skill
  cangjie.capability-count: 14
  cangjie.entrypoint-count: 8
---
# 精准择时——波浪理论实战策略 — 来源路由入口（compact pack）

## 触发与不触发

**适用**：与本书能力域相关的咨询与任务（见下方路由表的意图列）。
**不适用**：
- 纯基本面估值与财务分析
- 消息面、资金流、盘口与高频交易
- 无 K 线数据或流动性极差的品种
- 保证收益类承诺

## 核心原则（常驻速览，概览类问题读到这里即可回答）

1. 先定级定方向，再谈买卖点：级别判错则止损、目标、仓位全错
2. 「具备结构条件」不等于「结束信号」：前者只能主动出局/减仓，后者才能反向建仓
3. 三类交易点严格区分：逆势点（调整极端分批）、转势点（结束信号确认）、顺势点（趋势确立后回调结束）
4. 止损永远放本浪起点之外，目标放高一级结构条件处，主动/被动出局事先分设
5. 位置决定策略：同一形态在不同位置，目标、止损、仓位全不同
6. 多标注/多演变时不硬选边：等幅度大的结构具备条件、等验证、或降仓

## 能力路由（先读本表，按意图加载 1 张能力卡）

| 用户意图 | 先读 | 补读/备注 |
|---|---|---|
| 判断当前浪级与趋势方向；确定该看哪个周期；用突破确立高一级趋势；锚定基础浪与细分浪 | references/capabilities/wave-degree-and-direction-skill.md | 已晋级为独立 Skill `wave-degree-and-direction-skill`（已安装时优先直接使用；本卡仅作原文与背景补充） |
| 判断调整浪是否走完；区分结构条件与结束信号；判断能否抄底或反向建仓；处理结束点下移 | references/capabilities/structure-condition-vs-end-signal-skill.md | 已晋级为独立 Skill `structure-condition-vs-end-signal-skill`（已安装时优先直接使用；本卡仅作原文与背景补充） |
| 识别调整浪形态；判断调整会有多深；判断后续 C 浪强弱；区分剪刀/镰刀/双节棍 | references/capabilities/correction-pattern-dictionary-skill.md | 已晋级为独立 Skill `correction-pattern-dictionary-skill`（已安装时优先直接使用；本卡仅作原文与背景补充） |
| 判断这个低点能不能抄；区分逆势点/转势点/顺势点；制定分批建仓计划；设定止损链 | references/capabilities/countertrend-entry-and-trade-point-taxonomy-skill.md | 已晋级为独立 Skill `countertrend-entry-and-trade-point-taxonomy-skill`（已安装时优先直接使用；本卡仅作原文与背景补充） |
| 找多空分界点；判断破与不破怎么应对；处理标号上移下移；找天然止损位 | references/capabilities/bull-bear-divide-and-relabeling-skill.md | 已晋级为独立 Skill `bull-bear-divide-and-relabeling-skill`（已安装时优先直接使用；本卡仅作原文与背景补充） |
| 判断当前位置该用什么策略；决定仓位轻重；判断是顺势还是反弹 | references/capabilities/position-decides-strategy-skill.md | references/capabilities/wave-degree-and-direction-skill.md、references/capabilities/forecast-methods-skill.md、references/capabilities/trend-following-entry-skill.md |
| 找顺势买点；判断回调到哪里买；区分回调与反转；找加仓点 | references/capabilities/trend-following-entry-skill.md | 已晋级为独立 Skill `trend-following-entry-skill`（已安装时优先直接使用；本卡仅作原文与背景补充） |
| 止损放哪里；目标位多少；什么时候走；风险回报比怎么算 | references/capabilities/stop-target-and-exit-skill.md | 已晋级为独立 Skill `stop-target-and-exit-skill`（已安装时优先直接使用；本卡仅作原文与背景补充） |
| 短线能不能买；周线回调买点；短线买点类型判断 | references/capabilities/short-term-entry-patterns-skill.md | references/capabilities/countertrend-entry-and-trade-point-taxonomy-skill.md、references/capabilities/position-decides-strategy-skill.md、references/capabilities/structure-condition-vs-end-signal-skill.md |
| 哪个板块要启动；板块启动怎么选股；板块内选个股 | references/capabilities/sector-stock-selection-skill.md | references/capabilities/position-decides-strategy-skill.md、references/capabilities/high-probability-resonance-skill.md、references/capabilities/countertrend-entry-and-trade-point-taxonomy-skill.md |
| 有没有共振买点；多个买点挑最好的；仓位该多重 | references/capabilities/high-probability-resonance-skill.md | references/capabilities/countertrend-entry-and-trade-point-taxonomy-skill.md、references/capabilities/trend-following-entry-skill.md、references/capabilities/multi-timeframe-crosscheck-skill.md |
| 日线看不出方向怎么办；大级别转势怎么提前发现；多周期确认 | references/capabilities/multi-timeframe-crosscheck-skill.md | references/capabilities/wave-degree-and-direction-skill.md、references/capabilities/structure-condition-vs-end-signal-skill.md、references/capabilities/high-probability-resonance-skill.md |
| 两种数法都说得通怎么办；数浪纠结怎么下单；不确定时仓位怎么定 | references/capabilities/ambiguity-handling-skill.md | references/capabilities/wave-degree-and-direction-skill.md、references/capabilities/correction-pattern-dictionary-skill.md、references/capabilities/stop-target-and-exit-skill.md |
| 接下来会怎么走；能涨到哪；走势预测 | references/capabilities/forecast-methods-skill.md | references/capabilities/wave-degree-and-direction-skill.md、references/capabilities/position-decides-strategy-skill.md、references/capabilities/structure-condition-vs-end-signal-skill.md |

**非能力类查询**：
- 书名/作者/章节/整书概览 → references/overview.md
- 术语解释 → references/glossary.md
- 决策规则速查（不需要原文依据时） → references/cheatsheet.md
- 完整意图与关键词索引（本表未覆盖的意图先查这里） → references/capability-index.md

## 加载规则

- 每次任务先读本文件，再按路由表加载 **1** 张能力卡；任务明确跨域时最多加载 2 张。
- 概览/书名类问题不加载能力卡，用「核心原则」与 overview.md 回答。
- 路由表与 capability-index.md 都无法命中的意图，明确告知超出本书范围，不要硬套。

## 边界与判停

- 多周期数据不足（无法定级）时停止，要求补数据
- 结构标注存在多解且无法比较幅度时，只观察不参与
- 关键点位无法确定（浪起点不明）时，不下单
