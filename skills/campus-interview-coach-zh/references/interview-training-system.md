# Interview Training System

Use this file when the user asks for mock interview, interview training, drills, question bank practice, repeated practice, or high-quality coaching.

## Training stance

Do not optimize only for a perfect answer. Optimize for visible improvement.

The user should leave training with:
- clearer understanding of what the interviewer is testing
- one or two repeatable answer habits
- stronger follow-up resilience
- a record of what improved and what still fails under pressure

Default to active practice:
- ask one question
- wait for the user's answer
- diagnose the answer
- ask the user to re-answer with a constraint
- then raise difficulty with a follow-up

Only provide a full model answer first when:
- the user explicitly asks for one
- the user has no relevant material yet
- the user is blocked and asks for help
- the task is not practice, but rewrite or preparation

## Training modes

### 1. Baseline diagnosis

Use when the user says `先看看我什么水平`, `帮我诊断`, or gives one answer.

Output:
- current level by round standard
- top 2 failure modes
- strongest available material
- one training priority
- first drill question

### 2. Round-specific mock

Use when preparing for a specific round.

Question design:
- first round: project detail, ownership, execution, collaboration
- second round: judgment, priority, tradeoff, role fit, business logic
- HR/final: motivation-fit, values under tradeoff, stability, expectation alignment, reverse questions

Run:
- warm-up question
- project or motivation deep-dive
- pressure follow-up
- reverse-question or closing drill
- short scorecard

### 3. Deep-dive drill

Use when one project, internship, or story is central.

Drill sequence:
1. `30-second credibility`: what was the context, task, ownership, and result?
2. `ownership split`: what did the user personally do vs what the team did?
3. `method`: what tools, judgment, data, or process did the user use?
4. `obstacle`: what got hard and how did the user adapt?
5. `tradeoff`: what did the user choose not to do and why?
6. `reflection`: what changed in the user's thinking?
7. `round reframing`: tell the same story for first round, second round, and HR/final.

### 4. Competency drill

Use when the user has a clear weakness.

Common drill targets:
- `structure`: answer with conclusion -> evidence -> takeaway
- `ownership`: separate personal contribution from team output
- `depth`: explain method, judgment, and constraints
- `business judgment`: connect action to metric, user, or business outcome
- `motivation-fit`: explain choice standard and past evidence
- `self-awareness`: name weakness, correction method, and result
- `follow-up resilience`: handle challenge without defensiveness
- `reverse questions`: ask questions that reveal role understanding

Run 3 short cycles:
- question
- user answer
- one-sentence diagnosis
- re-answer instruction
- harder follow-up

### 5. Stress mock

Use when the user asks for pressure or has already passed basic drills.

Pressure types:
- challenge ownership: `这听起来更像团队结果，你个人贡献在哪里？`
- challenge motivation: `这家公司和别的公司有什么本质区别？`
- challenge tradeoff: `如果资源只有一半，你怎么取舍？`
- challenge consistency: `你刚才说想稳定，但又说想快速尝试新方向，这两个怎么统一？`
- challenge depth: `你这个方法为什么有效？有没有反例？`
- challenge risk: `如果我担心你来了以后发现不适合，你怎么回应？`

Rules:
- be firm but not humiliating
- challenge the answer, not the user
- after pressure, coach recovery language

## Feedback format

Keep feedback short enough that the user can re-answer immediately.

Default feedback:

```md
这题考点：

你这版最强：

最大风险：

改法：
- 开头先说：
- 中间补：
- 结尾落到：

请你重答一遍，限制：
```

Use scores lightly in live training:
- `relevance`
- `structure`
- `depth`
- `persuasion`
- `follow-up resilience`

Score only observable behavior. Do not score hidden quality.

## Re-answer constraints

Use one constraint at a time:
- `30 秒内先给结论`
- `必须说清楚你个人负责什么`
- `补一个取舍，不要只讲流程`
- `把背景压到两句话`
- `最后加一句复盘`
- `不要说“我们”，改成“我负责...”`
- `用一个具体指标或证据支撑`
- `回答里必须出现“为什么这个岗位”`
- `不要背稿，用自然口语讲`

## Difficulty ladder

Level 1: clarity
- can the user answer the question directly?
- can they avoid rambling?

Level 2: evidence
- does the answer include concrete action?
- can the user distinguish personal contribution from team output?

Level 3: reasoning
- does the user explain why they made choices?
- can they name tradeoffs and constraints?

Level 4: transfer
- can the user connect the story to the target role?
- can they reframe the same story for another round?

Level 5: pressure
- can the user handle doubts, contradictions, and edge cases calmly?

Do not jump to Level 5 if Level 1 or 2 is broken.

## Question generation rules

Good training questions are:
- round-specific
- based on the user's actual resume, JD, or stated weakness
- open enough to reveal thinking
- followed by one pressure probe

Avoid:
- dumping 20 questions without prioritization
- asking trick questions with no hiring signal
- giving only common internet questions
- training every weakness at once

## Training plans by time

### 10 minutes

Use:
- one baseline question
- one diagnosis
- one re-answer
- one pressure follow-up
- one next-step note

### 30 minutes

Use:
- 3 drill cycles
- one project deep-dive
- one motivation or reverse-question drill
- short progress log

### 60 minutes

Use:
- baseline scorecard
- project deep-dive
- round-specific mock
- pressure section
- reverse-question section
- final training log

## Progress log

At the end of a training block, summarize:

```md
## 训练记录
- 当前最稳能力：
- 本轮修正成功：
- 仍然危险：
- 下次优先练：
- 推荐下一题：
```

If continuing across turns, start from the last `仍然危险` and `下次优先练`.

## Quality guardrails

High-quality training should not:
- over-polish the user's voice until it sounds fake
- invent stronger evidence than the user gave
- bury the user in frameworks
- make every answer longer
- praise without requiring a better second attempt
- treat all roles as product/strategy roles

High-quality training should:
- make the user answer first whenever possible
- preserve truthful uncertainty
- convert vague claims into visible behavior
- help the user survive follow-up questions
- make each round's bar explicit
