# Stage 4 压力测试摘要

> 本文件按仓库根 `test-results.md`、`single/` 与 `pack/` 入口目录下的 `test-prompts.json` 以及仓库内实际文件整理，只做归纳与结构核对，不新增、不改写任何判卷结论；统计数字均为脚本实测（2026-10-29）。

## 测试范围

- **技能包规模**：仓库内共 9 个 skill 目录，对应两种安装变体 —— `single/` 下 1 个入口技能（`wave-accurate-timing-skill`，装 1 个可发现入口）；`pack/` 下 8 个（1 个 router `wave-accurate-timing-skill-router` ＋ 7 张独立能力 skill：`wave-degree-and-direction-skill`、`structure-condition-vs-end-signal-skill`、`correction-pattern-dictionary-skill`、`countertrend-entry-and-trade-point-taxonomy-skill`、`bull-bear-divide-and-relabeling-skill`、`trend-following-entry-skill`、`stop-target-and-exit-skill`，合起来 8 个可发现入口，与阶段 1.6 晋级门的预算一致）。单入口包内另有 14 张能力卡（`single/wave-accurate-timing-skill/references/capabilities/`）。
- **test-prompts 文件数**：实测仓库内共 2 个 `test-prompts.json`，均为入口级 suite（同一份用例的两处副本，文件名不含 skill 名）：
  - `single/wave-accurate-timing-skill/test-prompts.json`
  - `pack/wave-accurate-timing-skill-router/test-prompts.json`（router 副本；用例与上者相同，`skill` 字段为 router 名）
  `pack/` 下 7 个晋级 skill 目录暂无各自的 test-prompts.json（仓库内没有按能力拆分的用例，未补造）。
- **用例条数**：单个文件 9 条，两个文件合计 18 条（去重后仍为同一份 9 条用例集）。按 type 统计：`should_trigger` 6 条、`should_not_trigger` 6 条、`edge_case` 6 条、`output_case` 0 条；单文件为 3 / 3 / 3 / 0。
- **用例外的真实任务用例**：另有 2 条真实任务输出用例 T7（顺势点）／T8（剪刀式二次分解），只以归档中的 `.md` 输出文件形式保留（T7-output.md、T8-output.md），未写进 `test-prompts.json`，因此不在本仓库内。
- **覆盖面**：触发（正例）／跨技能误触发（诱饵：基本面估值、单纯数浪、道氏理论）／边界（多标注不确定性、只有单周期数据、T+1 与涨跌停可执行性）／输出（T7、T8 的完整分析产出）。

## 结构检查

在仓库根执行，逐项实测（2026-10-29）：

| 检查项 | 结果 |
|---|---|
| JSON 可解析性 | 5 / 5 通过（`single/.../test-prompts.json`、`pack/.../test-prompts.json`、`single/.../BUILD_MANIFEST.json`、`pack/BUILD_MANIFEST.json`、`pack/capability-destinations.json`），逐个 `json.load` 验证，无解析失败 |
| `test-prompts.json` 字段完整性 | 通过：两个文件均含 `skill` / `version` / `source` / `note` / `test_cases`；每个文件各 9 条用例，均具备 `id` / `type` / `prompt` / `expected_behavior` / `notes` |
| SKILL.md frontmatter | 9 / 9 通过：9 个 skill 目录的 `SKILL.md` 均有 YAML frontmatter，且 `name` 字段与所在目录名一致 |
| 能力卡六段完整性（R / I / A1 / A2 / E / B） | 14 / 14 通过：`single/wave-accurate-timing-skill/references/capabilities/` 下 14 张卡六段标题齐全，无缺段 |
| 用例类型覆盖 | 3 类齐全（`should_trigger` / `should_not_trigger` / `edge_case`），各 3 条；`output_case` 0 条（T7 / T8 尚未转成用例条目） |

## 结果

- skills: 9（single 1 ＋ pack 8）
- test_json: 2 个文件（条目合计 18 条，去重后为同一份 9 条入口级用例集）
- 通过情况（照仓库根 `test-results.md` 原文转述，未做二次统计）：
  - **首轮（2026-10-18，独立盲测代理）**：正例 3 / 3 正确触发并正确执行；诱饵 3 / 3 未触发，其中跨技能混淆 2 / 2 正确转出（转 `wave-accurate-counting-skill`、`dow-theory-classic-skill`）；边界 2 / 2 判定合理，第 3 条 edge-03（T+1 可执行性）当批未单独实测，记为待补测。
  - **真实任务输出**：T8 与能力卡 E 段步骤逐条对应、术语正确；T7 因场景本身缺「60 分调整浪低点」，止损按规则判停、不猜价位——记录的是「卡住的地方」，不是「通过」。
  - **复核修复轮（2026-10-24，独立复核代理）**：edge-03 补测通过；T7 补 60 分低点（16.95）后复算，止损 16.88、目标 18.20（假设已注明）、风险回报比约 1.5:1；双 skill 近邻负例 4 / 4 单选无双重触发；触发套件复测 8 / 9，唯一分歧是「单纯数浪」在未安装《精准数浪》的环境下由本技能接住；R 段引文逐字核对 38 / 38。
  - **口径说明**：归档与仓库均未给出单一汇总「通过率」数字，本文件也不推算；上述分项即归档记录的全部结果，遗留项记为无。

## 可接入 darwin-skill 的后续动作

- **作为回归样本**：`test-prompts.json` 的 9 条用例是 darwin-skill 兼容格式（`type` / `expected_behavior` / `notes` 在盲测时对被测代理隐藏），可直接作为本技能的固定回归集；每次改 `SKILL.md` 路由表或改能力卡判停规则后重跑这 9 条，重点看正例是否仍正确加载对应能力卡、诱饵是否仍不外溢。
- **补强负例**：复核轮已验证与《精准数浪》的双 skill 近邻负例 4 条，建议把这 4 条正式写进 `test-prompts.json`（当前只存在于 test-results 的记录中），让「双触发为零」变成可重复执行的用例。
- **补齐输出用例**：T7 / T8 目前是散落在归档里的 `.md` 输出，建议改为带固定输入的 `output_case` 用例条目，使止损/目标/风险回报比这类输出判定也能自动比对。
- **挂账项转用例**：edge-03 已补测通过，但其「纯价格止损判停 + 仓位上限/预埋条件单/弃做三项替代」的期望行为尚未写进 `expected_behavior`，接入时应补上，否则后续重跑无法判卷。
- **已知判停边界**：T7 首轮暴露的是用例设计缺口（未给 60 分调整浪低点），接入时应修正输入而不是放宽判卷标准。
