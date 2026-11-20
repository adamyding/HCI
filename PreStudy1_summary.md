# Pre-Study 1: Human-to-AI Knowledge Transfer in Existing Logs

## Main Goal

Understand what human-to-AI knowledge transfer looks like in real conversations and whether it can be objectively measured.

Using StudyChat and RealCompanion to:
1. Identify: What types of knowledge do humans provide to AI?
2. Observe: How does AI respond to, retain, and reuse that knowledge?
3. Categorize: Distinguish recall, application, and potential knowledge transfer.
4. Assess: Can these behaviors be reliably identified and quantified using existing datasets?

## Data and method

| | StudyChat | RealCompanion |
|---|---|---|
| Setting | Students using an AI assistant in an undergraduate AI course | 10 people's long-term use of a companion app |
| Size | 2,214 chats, 203 students | 1,624 sessions, 12,795 user messages |
| AI memory across conversations | None | Unknown |

1. **Knowledge:** code what each human turn gives the AI (correction, constraint, teaching, personal fact).
2. **Opportunity:** for each later task, judge whether the earlier knowledge was needed, *before* looking at the AI's reply.
3. **Outcome:** check whether the AI used it, and whether the human had to repeat it.

Rates are **per opportunity**: of the times the knowledge should have mattered, how often was it used?

## 1. Identify: what knowledge do people give?

**People give knowledge often, but rarely teach.**

| | StudyChat | RealCompanion |
|---|---|---|
| Turns containing knowledge | 17% | 69% |
| Main kind | Task facts, corrections, constraints | Personal facts |
| Deliberate teaching | 1.3% | 0.2% |

- *e.g. knowledge (a correction):* *"Please try again, and use the column "Target_ckd""*
- *e.g. teaching:* *"You need to take the frequency inverse and sum them together at each node. Whatever gives the least cost is selected first from the priority queue"*
- Durable knowledge (e.g. standing rules, personal facts) matters later more often than one-off details: 39% vs 28%.

## 2. Observe: does the AI reuse it?

**Yes when the knowledge is visible. Across sessions it depends on the system.**

| Pattern | Used without a reminder | Used after the human repeats it |
|---|---|---|
| Same chat (knowledge still in view) | 80% | — |
| New chat (no memory) | ≈0% (1 of 61) | 36 of 38 |
| Companion app, later session | 63% (upper bound) | 94% |

- *e.g. same chat:* after the `Target_ckd` correction, the student asks two tasks later to *"Describe the features of the dataset"*; the AI lists `Target_ckd` without a reminder.
- *e.g. new chat:* a student asked for *"one short paragraph"* in one chat; in a later chat the AI writes at length until the student repeats *"explain in just 3-4 lines"*.
- Earlier knowledge is relevant to a later task in **32%** of cases within a chat and **48%** in the companion app (vs 4–6% for random pairs).
- **Main failure (StudyChat): ignoring it (19%)**, mostly earlier constraints the user expected to keep holding.
- Wrong use is rare (<2%).
- Companion-app reuse does not fade over 90 days.
- The companion-app 63% is an upper bound: we only checked whether the user repeated the knowledge inside the later conversation, not in sessions in between.

## 3. Categorize: recall, application or transfer?

**Mostly applying knowledge in the same form. Far transfer never appeared.**

| What the later task needed | StudyChat | RealCompanion |
|---|---|---|
| Recall it | 2% | 36% |
| Apply it as is | 80% | 43% |
| Adapt it | 18% | 21% |

- *e.g. recall:* the companion refers back to something the user mentioned in an earlier session (RealCompanion; described generally, per the data-use agreement).
- *e.g. apply as is:* the corrected `Target_ckd` column is used in a later task.
- *e.g. adapt:* a student says autocomplete must return every completion of a prefix, not just the first word; when they later ask *"could you write it again but with a DFS appraoch"*, the AI's new DFS code still returns all completions.
- **Far transfer** (a principle applied to a structurally different problem) was never observed.
- Cross-topic reuse does occur, but it carries a preference or personal fact into a new topic, not a principle into a new problem. *e.g.* a "keep answers brief" preference carried into a question on a different topic.

## 4. Assess: can chat measure this reliably?

**Partly. Basic reuse numbers are trustworthy, deeper ones are shaky, and some questions can't be answered from chat data.**

Checked by how often two AI annotators (Claude Haiku and Sonnet) agree: κ, where 0 = chance, 1 = perfect, 0.6+ = good. No human check yet.

- **Trustworthy:** whether earlier knowledge was needed (κ 0.62–0.69); whether the AI used it in StudyChat (κ 0.66).
- **Shaky:** whether the AI used it in RealCompanion (κ 0.38); adapted or conceptual use (40–59% can't be judged).
- **Not answerable:**
  - whether the AI could see the knowledge (memory vs long context);
  - reuse vs coincidence (*e.g.* a new chat left a student's main function alone without knowing that was their rule);
  - how long an instruction was meant to hold (*e.g.* *"dont provide code"*: for one question, or the whole chat?);
  - far transfer (never occurs naturally).

## Potential framework (draft)

**Definition** (tbd) Knowledge transfer: knowledge a human gives the AI (K) improves the AI's answer in a later task.

**Dimensions** (tbd):
- **Kind of knowledge:** fact, rule, concept
- **Scope:** one-off (for this question only) or standing (meant to keep holding)
- **Task distance:** near (same form) to far (structurally different problem)
- **Time:** same chat, later session, weeks later

**Components** (sample)(example: chat 1655)

| Component | What we examine | Example |
|---|---|---|
| 1. Knowledge identification | What did the human provide? Is it correct? | A correction: `Target` became `Target_ckd` (correct) |
| 2. Opportunity | Does K matter for a later task? Judged *before* looking at the AI's answer | *"Describe the features of the dataset"* needs it: yes |
| 3. Knowledge use | What did the AI do with K? Used / adapted / ignored / misused / outdated / over-applied | Uses `Target_ckd` |
| 4. Transfer assessment | Was it because of K? (with vs without K) | Can't be tested from the chat. A with/without-K run would check whether the AI says `Target` without K |

**Access** is recorded for every case: was K still visible, held in memory, or repeated by the human? Without it, recall and repetition can't be separated from transfer.
