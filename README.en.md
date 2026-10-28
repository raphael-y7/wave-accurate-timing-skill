<h1 align="center">Wave Accurate Timing Skill</h1>

<p align="center"><a href="README.md">中文</a> | English</p>

An AI skill pack for immediate use — it distills the internal-wave-structure timing method from 陈晓东's *Accurate Timing: Wave Theory Practical Strategy* into 14 capability cards that can be triggered individually or combined.

It is not a book summary, nor a reading response — it breaks the reusable methodology in the book into skill modules that can be triggered, executed and tested.

## What these skills solve

- Talking about entries before fixing the degree: which wave degree is running, which way it points, which timeframe to read — settle that first, or every stop, target and position size downstream is wrong
- Mistaking "the correction is finished" for "the reversal is confirmed": a complete `{a}{b}{c}` only means the structure *may* end; it can still extend into scissors, sickle, nunchaku or a wave-within-a-wave and drag the higher-degree end point down with it — this is where most heavy-size bottom-fishing goes wrong
- Whether this low can be bought, whether it is a countertrend point, a turn point or a trend-following point, how large the first tranche should be, and whether to add on the way down
- Where the stop goes, where the target sits, when to exit by plan, when to exit on a signal, and how the stop ratchets up
- Where the bull/bear dividing line is, what to do when it holds versus breaks, and whether a label should be moved up or down
- When two wave counts both look valid, when the daily chart gives no direction, or when several entry points appear at once — how to size and how to act

## What was distilled

14 capability cards, organized in the order "fix degree and direction first, judge whether the structure has ended second, land on entries and exits last":

- **Degree and structure** (3): `wave-degree-and-direction-skill` (degree and direction), `structure-condition-vs-end-signal-skill` (structure condition vs end signal), `correction-pattern-dictionary-skill` (correction pattern dictionary: scissors, sickle, nunchaku and four special structures)
- **Locating trade points** (4): `countertrend-entry-and-trade-point-taxonomy-skill` (countertrend bottom-fishing and the trade-point taxonomy), `bull-bear-divide-and-relabeling-skill` (the bull/bear dividing line and relabeling), `trend-following-entry-skill` (trend-following points), `short-term-entry-patterns` (short-term entries)
- **Risk and exits** (1): `stop-target-and-exit-skill` (stop, target and exit)
- **Position, confluence and cross-checks** (4): `position-decides-strategy` (position decides strategy), `high-probability-resonance` (high-probability structures and three-level confluence), `multi-timeframe-crosscheck` (multi-timeframe cross-check), `ambiguity-handling` (multiple counts and uncertainty)
- **Stock selection and forecasting** (2): `sector-stock-selection-skill` (picking stocks when a sector turns up), `forecast-methods` (forecasting methods)

## Two packaging modes: single and pack

The same 14 capability cards are compiled twice, at two granularities. The content is identical; the only difference is how many entries an agent can discover.

| | single (one entry) | pack (compact pack, multiple entries) |
|---|---|---|
| Discoverable entries | **1**: `wave-accurate-timing-skill` | **8**: one source router + 7 promoted standalone skills |
| Where the 14 cards live | All inside the entry's `references/capabilities/`, loaded one at a time (at most two when the task crosses domains) by the router table | 7 high-frequency cards become standalone skills; the other 7 stay in the router's `references/` |
| Triggering | Only the entry description participates in matching; routing happens after entry | The 7 high-frequency capabilities are matched directly, one hop fewer |
| Upgrades | Replace 1 directory | Replace 8 directories |

The 7 cards promoted to standalone skills in the pack:

- `wave-degree-and-direction-skill` — degree and direction
- `structure-condition-vs-end-signal-skill` — structure condition vs end signal
- `correction-pattern-dictionary-skill` — correction pattern dictionary
- `countertrend-entry-and-trade-point-taxonomy-skill` — countertrend bottom-fishing and the trade-point taxonomy
- `bull-bear-divide-and-relabeling-skill` — the bull/bear dividing line and relabeling
- `trend-following-entry-skill` — trend-following points
- `stop-target-and-exit-skill` — stop, target and exit

### Which one to install

Pick by the way you work, and **install only one**:

| How you work | Recommended | Why |
|---|---|---|
| You use DSH / Codex / Claude Code with a skills directory and want a clean list | single | Takes 1 slot, loses no capabilities |
| Your daily questions concentrate on "what degree is this / can I buy this low / stop and target / what correction pattern is this / where is the dividing line / pullback entries" | pack | Those are exactly the promoted standalone skills, matched directly |
| You distribute to several agents or teammates who pick what they need | pack | They can install only the standalone skills they want |
| You want to install once and maintain one directory | single | Upgrades replace a single directory |

> Both builds come from the same bundle and carry identical capabilities. **Installing both will double-trigger**, so pick one.

## Examples

### Example 1: a correction has become a "double-decomposed scissors" — can I buy this low?

**User question**

"This correction has turned into a double-decomposed scissors pattern, and the `{c}` has moved down again to 15.40. Can I buy the bottom now? Where does the stop go?"

**How the skill reasons**

- `structure-condition-vs-end-signal-skill`: separate "structure condition met" from "end signal" first — a complete `{a}{b}{c}` only means the structure *may* end and can keep evolving; it takes a lower-degree three-wave reversal that **verifies and closes beyond** the key low/high to count as an end signal
- `countertrend-entry-and-trade-point-taxonomy-skill`: with the condition met but no end signal, this point can only be classified as a countertrend point; and a countertrend point requires a settled higher-degree direction — with the direction unknown, observation only
- `stop-target-and-exit-skill`: the stop goes outside the origin of this wave, i.e. below the `{c}` low at 15.40; entries are tranched and each tranche carries its own stop

**Sample answer**

> Short answer: this point is a countertrend point, not a bottom.
>
> Layer one: a complete `{a}{b}{c}` only means "structure condition met". The book defines it as "may end", not "has ended" — it can still evolve into a sickle, a nunchaku or even a wave-within-a-wave, dragging the end point further down. To become a turn point you can size against, you need both a lower-degree three-wave reversal and a verified close beyond the key high. One without the other does not count.
>
> Layer two: even as a countertrend point, there is a precondition — the higher-degree direction must be settled first. You gave me the daily correction only, not where the weekly is heading. By the rules, with the higher-degree direction unknown the only allowed action is observation, not building a position.
>
> Layer three: the stop has no second formula — outside the `{c}` low at 15.40. "It has fallen enough" is not a reason to move the stop closer. How big the first tranche is depends on your risk preference: the book only asks for tranching and **gives no standard ratio**; the card's suggested ceiling is one third for the first tranche, adding at the `{b}`-moved-down / `{c}`-moved-down extremes, each tranche with its own stop.
>
> Two boundaries stated as they are: first, the book gives no quantitative tolerance for "verified close" (how far beyond the key level counts), so you must define it and write it into your plan; second, under A-share T+1 a same-day break of 15.40 cannot be executed that day, and a limit-down gap can jump straight through the stop.

### Example 2: a trend-following pullback — can I buy, and what goes in the stop and target fields?

**User question**

"The weekly C broke above the A high at 21.30. The daily corrected `{a4}` 15.80, `{b4}` 18.20, `{c4}` 16.35 without breaking `{a4}`. On the 60-minute chart, (a) broke above the (b)-moved-down high at 17.40 and the pullback closed above 16.90. Can I buy now? Where is the stop, and what is the target?"

**How the skill reasons**

- `trend-following-entry-skill`: a trend-following point needs three conditions — the higher-degree trend is established (weekly C above the A high at 21.30), the current-degree correction printed an end signal (60-minute (a) above the (b)-moved-down high at 17.40, verified close above 16.90), and the correction low did not break the prior key low (16.35 above 15.80). All three must hold
- `stop-target-and-exit-skill`: the stop goes **outside the origin of this wave** — this trade rides the 60-minute correction, so the stop belongs below the 60-minute correction low; the target sits where the higher-degree wave meets its structure condition, not at a fixed percentage; planned exit and signal exit are set separately; the stop only ratchets up, never down
- Missing inputs are asked for, not guessed: the 60-minute correction low and the internal structure of the weekly leg are both absent

**Sample answer**

> By classification this is a trend-following point, not bottom-fishing: the weekly C above the A high at 21.30 settles the higher-degree trend, the daily correction 15.80 → 18.20 → 16.35 did not break `{a4}`, and the 60-minute (a) broke the (b)-moved-down high at 17.40 and verified a close above 16.90. All three conditions hold.
>
> But I cannot fill the stop field. The rule is "outside the origin of this wave", and this trade rides the 60-minute correction — so the stop belongs below the 60-minute correction low, while the only low you gave me is the daily 15.80. Using 15.80 as the stop means using a higher-degree low as your stop, and the card states plainly that this makes risk uncontrollable. So give me one number first: what is the low of this 60-minute correction.
>
> The target cannot be invented either: it is "where the higher-degree wave meets its structure condition", which needs the internal structure of the weekly leg you did not provide. Left blank for now.
>
> Once those two numbers arrive, write three things down before entering: the planned exit (leave when the target structure is reached), the signal exit (leave when a reversal signal appears), and the stop migration rule (as price advances, the stop only moves up, never down). Note also that "acceptable stop distance" is a qualitative judgement in the book with **no numeric standard**, so set it from your own risk preference and put it in the plan.

## How these skills were generated

These skills were produced with the **[cangjie-skill](https://github.com/kangarooking/cangjie-skill)** RIA-TV++ pipeline, in six stages:

1. **Whole-book comprehension (Adler analysis)** — apply Mortimer Adler's analytical reading method to the book: structure, interpretation, criticism, application
2. **Parallel extraction** — several specialized extractors (frameworks, principles, cases, counter-examples, terminology) mine candidate methodology units from the source text
3. **Triple verification** — every candidate must pass three checks: at least two independent in-book supports (cross-domain), the ability to answer questions the book never explicitly addresses (predictive power), and not being common sense (distinctiveness)
4. **RIA++ construction** — structure each unit along R (quotation) / I (restatement in own words) / A1 (in-book case) / A2 (future trigger scenario) / E (executable steps) / B (boundaries and blind spots)
5. **Zettelkasten linking** — map dependencies, contrasts and combinations between cards, producing the capability index and routing table
6. **Trigger and output testing** — write trigger blind tests (including decoy questions: fire when they should, stay silent when they should not) and output evaluation scenarios for every card; failing cards go back for rework and are re-verified afterwards

The hard part of distilling this book was keeping "what the author claims" separate from "how strong the evidence is": every chart in the book is a retrospectively labeled move already in the past, and there is not one complete account review that includes losing trades; key criteria such as "verified close" carry no quantitative tolerance in the book. So every card carries a boundaries-and-blind-spots section that separates "what the book says" from "how far to trust it and where it breaks".

## Testing and verification

This repository publishes the test material from the generation process alongside the skills: `evals/test-prompts.json` is the fixed case suite, and `evals/test-results.md` holds the item-by-item scoring plus the follow-up round — methods, per-category verdicts, and the cases left untested, not a single line saying "all passed".

- **Blind-test method**: an independent blind-test agent (not involved in the distillation) received only the skill path and the user request, first had to decide "will it trigger, which card loads", then actually executed the full analysis and wrote it to a file; neighbouring skills (the author's wave-counting skill, a wave-theory skill and a Dow-theory skill) were supplied as confusors
- **Case count**: `evals/test-prompts.json` holds 9 cases = 3 should-trigger + 3 decoys + 3 edge cases; plus 2 real task-output cases (T7 / T8)
- **Trigger verdicts** (as recorded in `evals/test-results.md`): should-trigger 3 / 3 fired and executed correctly; decoys 3 / 3 stayed silent (2 of them correctly handed off to neighbouring skills); edge cases 2 / 2 judged reasonably, while the third (T+1 executability) was not tested on its own in that batch and was booked as pending
- **Output verdicts**: T8 maps step by step onto the card's section E; T7, because the scenario itself lacked the 60-minute correction low, stopped at the stop field instead of guessing a price — the record keeps "where it got stuck", not only "what passed"
- **Follow-up round** (2026-10-24): edge-03 passed on retest; T7 recomputed after supplying the 60-minute low — stop 16.88, target 18.20 (the assumption is stated), risk-reward about 1.5:1; four neighbouring-skill negative cases went 4 / 4 single-select with no double trigger; the trigger suite retested at 8 / 9, the single disagreement being that "just count the waves" was caught by this skill in an environment where the counting skill was not installed; section-R quotations were checked word by word at 38 / 38
- **Open items and accounting**: none recorded as outstanding; this repository did not reconcile the counts, did not rewrite any verdict, and derives no pass rate from them

## Repository layout

```text
wave-accurate-timing-skill/
├── README.md                      ← Chinese version
├── README.en.md                   ← you are reading this
├── LICENSE                        ← MIT
├── BOOK_OVERVIEW.md               ← whole-book comprehension (Adler four-step, stage 0 output)
├── verified.md                    ← triple-verification conclusions and follow-up review
├── INDEX.md                       ← skill map: capability table + dependencies + loading order
├── TEST_SUMMARY.md                ← stage 4 pressure-test summary: case inventory / structure checks / results
├── CANGJIE_ADAPTATION.md          ← cangjie adaptation note: text status / distillation goals / evidence rules / scope limits
├── candidates/                    ← stage 1 candidate pool (5 types × 8 chunks + whole-book merge, 45 text files)
│   ├── cases.md                   ← case type, whole-book merge
│   ├── cases-chunk01.md
│   ├── cases-chunk02.md
│   ├── cases-chunk03.md
│   ├── cases-chunk04.md
│   ├── cases-chunk05.md
│   ├── cases-chunk06.md
│   ├── cases-chunk07.md
│   ├── cases-chunk08.md
│   ├── counter-examples.md        ← counter-example type, whole-book merge
│   ├── counter-examples-chunk01.md
│   ├── counter-examples-chunk02.md
│   ├── counter-examples-chunk03.md
│   ├── counter-examples-chunk04.md
│   ├── counter-examples-chunk05.md
│   ├── counter-examples-chunk06.md
│   ├── counter-examples-chunk07.md
│   ├── counter-examples-chunk08.md
│   ├── frameworks.md              ← framework type, whole-book merge
│   ├── frameworks-chunk01.md
│   ├── frameworks-chunk02.md
│   ├── frameworks-chunk03.md
│   ├── frameworks-chunk04.md
│   ├── frameworks-chunk05.md
│   ├── frameworks-chunk06.md
│   ├── frameworks-chunk07.md
│   ├── frameworks-chunk08.md
│   ├── glossary.md                ← glossary type, whole-book merge
│   ├── glossary-chunk01.md
│   ├── glossary-chunk02.md
│   ├── glossary-chunk03.md
│   ├── glossary-chunk04.md
│   ├── glossary-chunk05.md
│   ├── glossary-chunk06.md
│   ├── glossary-chunk07.md
│   ├── glossary-chunk08.md
│   ├── principles.md              ← principle type, whole-book merge
│   ├── principles-chunk01.md
│   ├── principles-chunk02.md
│   ├── principles-chunk03.md
│   ├── principles-chunk04.md
│   ├── principles-chunk05.md
│   ├── principles-chunk06.md
│   ├── principles-chunk07.md
│   └── principles-chunk08.md
├── bundle/                        ← distillation intermediates (auditable)
│   ├── verified.yaml              ← full spec of the 14 capability units (single source of truth)
│   ├── cards/
│   │   ├── ambiguity-handling-skill.md
│   │   ├── bull-bear-divide-and-relabeling-skill.md
│   │   ├── correction-pattern-dictionary-skill.md
│   │   ├── countertrend-entry-and-trade-point-taxonomy-skill.md
│   │   ├── forecast-methods-skill.md
│   │   ├── high-probability-resonance-skill.md
│   │   ├── multi-timeframe-crosscheck-skill.md
│   │   ├── position-decides-strategy-skill.md
│   │   ├── sector-stock-selection-skill.md
│   │   ├── short-term-entry-patterns-skill.md
│   │   ├── stop-target-and-exit-skill.md
│   │   ├── structure-condition-vs-end-signal-skill.md
│   │   ├── trend-following-entry-skill.md
│   │   └── wave-degree-and-direction-skill.md
│   └── book/
│       ├── overview.md            ← book overview
│       └── glossary.md            ← glossary
├── single/                        ← single-entry build
│   └── wave-accurate-timing-skill/
│       ├── SKILL.md               ← entry: triggers + router table + loading rules
│       ├── BUILD_MANIFEST.json    ← build manifest and file hashes
│       ├── test-prompts.json      ← 9 fixed cases (copy shipped with the skill, same content as evals/)
│       └── references/
│           ├── overview.md        ← book overview
│           ├── capability-index.md  ← full intent and keyword index (all 14 cards)
│           ├── cheatsheet.md      ← decision-rule quick reference
│           ├── glossary.md        ← glossary
│           └── capabilities/      ← the 14 capability cards
│               ├── ambiguity-handling.md
│               ├── bull-bear-divide-and-relabeling-skill.md
│               ├── correction-pattern-dictionary-skill.md
│               ├── countertrend-entry-and-trade-point-taxonomy-skill.md
│               ├── forecast-methods.md
│               ├── high-probability-resonance.md
│               ├── multi-timeframe-crosscheck.md
│               ├── position-decides-strategy.md
│               ├── sector-stock-selection-skill.md
│               ├── short-term-entry-patterns.md
│               ├── stop-target-and-exit-skill.md
│               ├── structure-condition-vs-end-signal-skill.md
│               ├── trend-following-entry-skill.md
│               └── wave-degree-and-direction-skill.md
├── pack/                          ← multi-entry build (compact pack)
│   ├── BUILD_MANIFEST.json
│   ├── capability-destinations.json
│   ├── wave-accurate-timing-skill-router/
│   │   ├── SKILL.md               ← source router entry
│   │   └── references/            ← the 14 cards + index, called internally by the router
│   │       ├── overview.md
│   │       ├── capability-index.md
│   │       ├── cheatsheet.md
│   │       ├── glossary.md
│   │       └── capabilities/
│   │           ├── ambiguity-handling.md
│   │           ├── bull-bear-divide-and-relabeling-skill.md
│   │           ├── correction-pattern-dictionary-skill.md
│   │           ├── countertrend-entry-and-trade-point-taxonomy-skill.md
│   │           ├── forecast-methods.md
│   │           ├── high-probability-resonance.md
│   │           ├── multi-timeframe-crosscheck.md
│   │           ├── position-decides-strategy.md
│   │           ├── sector-stock-selection-skill.md
│   │           ├── short-term-entry-patterns.md
│   │           ├── stop-target-and-exit-skill.md
│   │           ├── structure-condition-vs-end-signal-skill.md
│   │           ├── trend-following-entry-skill.md
│   │           └── wave-degree-and-direction-skill.md
│   ├── wave-degree-and-direction-skill/
│   │   └── SKILL.md
│   ├── structure-condition-vs-end-signal-skill/
│   │   └── SKILL.md
│   ├── correction-pattern-dictionary-skill/
│   │   └── SKILL.md
│   ├── countertrend-entry-and-trade-point-taxonomy-skill/
│   │   └── SKILL.md
│   ├── bull-bear-divide-and-relabeling-skill/
│   │   └── SKILL.md
│   ├── trend-following-entry-skill/
│   │   └── SKILL.md
│   └── stop-target-and-exit-skill/
│       └── SKILL.md
└── evals/                          ← trigger blind tests and output evaluation material
    ├── test-results.md             ← item-by-item scoring and follow-up round
    └── test-prompts.json           ← 9 fixed cases (3 trigger / 3 decoy / 3 edge)
```

## How to use

Clone the repository first:

```bash
git clone https://github.com/raphael-y7/wave-accurate-timing-skill.git
```

### Install single (try this first)

```bash
# macOS / Linux
cp -r wave-accurate-timing-skill/single/wave-accurate-timing-skill ~/.agents/skills/
```

```powershell
# Windows
Copy-Item -Recurse .\wave-accurate-timing-skill\single\wave-accurate-timing-skill "$env:USERPROFILE\.agents\skills\"
```

### Install pack

Copy only the directories that contain a `SKILL.md`; do not copy the two json files under `pack/` into your skills directory:

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

> `~/.agents/skills` is the DSH skills directory; with another agent, use its own directory (for example `~/.claude/skills` for Claude Code).

### How to check the install

Ask "this correction moved the `{c}` down again to 15.40 — can I buy the bottom, where is the stop", and see whether the agent separates "structure condition met" from "end signal", classifies the point as countertrend, and puts the stop below 15.40 — rather than simply telling you "you can scale in". With single installed it reads the entry and follows the router table; with pack installed, `structure-condition-vs-end-signal-skill` and `stop-target-and-exit-skill` are matched directly by their descriptions.

## Source

- *Accurate Timing: Wave Theory Practical Strategy* by 陈晓东
- Distilled from the whole book, producing 14 capability cards

## Disclaimer

This repository publishes only the distilled skills, indexes and quick-reference rules. It contains no PDF, EPUB, OCR file, screenshot or full transcript of the book. Quotations that appear in the cards serve only to attribute the methodology and keep it auditable.

Every criterion in the book (the tolerance of a "verified close", tranche ratios, acceptable stop distance, confluence conditions, sector-turn conditions and so on) is an induction from cases and experience; the book offers no statistical back-test, and several thresholds are not given at all. Test them on your own instruments and state the convention you use. Nothing in this repository is investment advice.

## License

[MIT](./LICENSE)
