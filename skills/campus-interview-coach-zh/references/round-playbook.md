# Round Playbook

Use this file when you need sharper round-specific judgment.

## Default round model

This is a heuristic, not a rule. Override it if the user gives explicit company information.

| Round | Typical interviewer | Core hiring question | Strong signals | Common fail pattern |
| --- | --- | --- | --- | --- |
| 一面 | future teammate, mentor, direct IC | `这个人能不能很快接活并且不拖后腿？` | resume is credible, actions are clear, can explain work end to end, basic communication is stable | vague responsibilities, weak ownership, cannot explain details, bloated self-description |
| 二面 | hiring manager, team lead, skip-level lead | `我愿不愿意把 headcount 用在这个人身上并向上负责？` | judgment, prioritization, business understanding, role fit, motivation, ability to summarize patterns from experience | only talks execution, no tradeoffs, no reflection, weak motivation, generic company answer |
| 三面/HR | HRBP, director, broader leader | `这个人是不是低风险、可持续、组织内可合作的人？如果给 offer，他会不会做出成熟承诺？` | motivation-fit, values under tradeoff, stable but realistic commitment, self-awareness, communication maturity, sensible expectations | unstable plans, hidden constraints, compensation-first attitude, generic loyalty, inconsistent story, cannot explain choice criteria |

## Why second round often feels stricter

Use this explanation when the user says `为什么总挂二面` or `为什么一面过了二面挂了`.

Common reasons:
- the manager owns hiring risk more directly than a peer interviewer
- the manager is screening for judgment and fit, not just task execution
- passing first round proves the candidate is not obviously weak; second round shifts the bar upward
- the same answer that looked solid in first round can look shallow in second round

## What first-round answers usually need

Optimize for:
- clarity
- direct ownership
- concrete tasks, tools, stakeholders, deliverables
- proof that the candidate can get up to speed

Useful question clusters:
- resume walk-through
- project deep dive
- how you handled a concrete execution problem
- how you worked with others on deliverables
- what you actually did vs what the team did

## What second-round answers usually need

Raise the level from `我做了什么` to `我为什么这么做`.

Look for:
- how the candidate diagnosed the problem
- what options they considered
- what tradeoffs they made
- what metric or business logic mattered
- what they learned and would change next time
- why this role and team fit their path

Also check the candidate's self-logic:
- can they explain why each internship, project, major, or direction change happened?
- do their experiences show a growth curve rather than a random timeline?
- can they summarize their core working style or advantage in one sentence?
- can they connect past choices to the current role without sounding like they are forcing a story?

Strong follow-up prompts:
- `你为什么优先做这个？`
- `如果资源只有一半，你怎么取舍？`
- `这件事如果失败了，根因会是什么？`
- `你做的这个动作，和业务结果之间的关系是什么？`
- `如果换一个团队/阶段，这个方法还成立吗？`
- `你当时为什么选择这段实习？`
- `这几段经历之间有什么递进关系？`
- `如果当时还有别的机会，你为什么会选这个？`
- `你说对这个方向感兴趣，是哪段经历验证了这一点？`

Second-round red flags:
- speaks for the team without clarifying personal ownership
- describes actions but not thinking
- repeats internet-ready motivation answers with no team-specific evidence
- claims to be interested in the role but cannot explain the team's business
- overuses `领导让我做` and underuses `我判断`
- explains internship choices as accidental only, such as `投了就去了`
- gives career planning that is either empty (`先做着看`) or inflated (`三年经理五年总监`)
- treats hardship as the story, but cannot name the judgment, result, or lesson
- blames uncooperative colleagues, managers, or scarce resources without showing how they decomposed and pushed the problem

## What HR or final behavioral rounds usually need

Focus on:
- motivation-fit, not just motivation slogans
- timeline stability and offer-intention risk
- values under tradeoff, not abstract values
- collaboration, conflict handling, pressure handling
- self-awareness and consistency
- realistic expectations about the role, location, compensation, manager style, and career path
- whether the candidate can choose responsibly rather than say `我都可以`

Useful topics:
- why this company and not a competitor
- how long the candidate plans to stay or what they want to learn
- conflict, feedback, failure, pressure, and change
- what kind of environment helps them perform best
- how the candidate makes decisions when two good options conflict
- what would make the candidate decline an offer or become unhappy after joining

Strong HR/final answers usually contain:
- a real preference or choice standard
- one past experience that proves the preference is stable
- a tradeoff the candidate understands
- a boundary stated maturely, without entitlement or defensiveness
- a link back to the target role's actual working reality

Weak HR/final answers often sound like:
- `我很喜欢贵司平台`
- `我抗压能力很强`
- `我没有什么特别不能接受的`
- `我的职业规划是成为行业专家`
- `我想先学习，然后看公司安排`

These answers are weak because they hide the decision logic. Rewrite them by asking:
- `你到底在选择什么？`
- `这份工作满足了你哪个阶段需求？`
- `什么现实条件会让你做不好？`
- `你过去哪件事证明你不是随口说说？`

## Diagnostic shortcuts

Use these shortcuts while debriefing:

- If the answer is factually fine but still feels weak in second round, the likely gap is `level`, not `truth`.
- If the user keeps talking for a long time without stating a point, the likely gap is `structure`.
- If the answer sounds hardworking but generic, the likely gap is `fit`.
- If the answer sounds polished but unsupported, the likely gap is `credibility`.
- If the answer is detailed but still unconvincing, the likely gap is `business relevance`.
- If the answer cannot explain why a choice was made, the likely gap is `choice logic`.
- If every experience is described separately but no pattern emerges, the likely gap is `storyline coherence`.
- If the user says a challenge was hard only because others did not cooperate, the likely gap is `agency`.
- If the user says an event was memorable only because they worked late, the likely gap is `cognitive upgrade`.
- If the HR answer sounds safe but forgettable, the likely gap is `choice standard`.
- If the user says `我都可以`, the likely hidden risk is `unexamined constraint`.
- If the user asks only benefits/promotion questions in final round, the likely gap is `responsible commitment framing`.
- If the reverse question can be answered from the official website, it is not a high-signal final-round question.

## Reframing guidance by round

Use the same story differently:

- One round:
  Lead with what the task was, what you owned, what you delivered, and what result you proved.
- Two round:
  Lead with the problem judgment, why you chose one route over another, and what that says about how you think.
- HR round:
  Lead with what the experience says about how you choose opportunities, work with people under constraints, handle tradeoffs, and commit responsibly.

## Second-round self-logic prep model

Use this model when preparing a candidate for a manager round, ByteDance-style second round, or any interview that asks many `why did you choose` questions.

### Resume experience audit

For every internship or major project, require an answer to:
- `what the company / department / role was`
- `what the team was trying to accomplish`
- `what the user's direct task and ownership were`
- `what method, tool, data, or judgment the user used`
- `what obstacle appeared`
- `what result happened`
- `what the user learned or would change`

If a claim is team-level, rephrase it as contribution-level:
- weak: `我把转化率提升了 5%`
- safer: `这个项目最终转化率提升了 5%，我负责其中的用户分层和触达策略部分`

### Choice logic

Use `stage + need + opportunity + validation`:
- `当时我处在什么阶段`
- `我最想补什么认知、技能、场景或 ownership`
- `这份机会为什么匹配这个需求`
- `它最终验证了什么，或者让我修正了什么`

Good second-round answers do not need to make every choice look perfectly planned. They need to show that the candidate can now reflect honestly and extract a pattern.

### Career storyline

Build a single line through the user's experiences:
- `起点`: what first exposed the user to the domain or role
- `验证`: which project or internship proved the interest or ability was real
- `聚焦`: what the user now knows they are relatively good at
- `目标`: why the target role is a reasonable next step

The strongest version sounds self-aware, not over-scripted.

### Story types worth preparing

Prepare at least one story for each:
- `from 0 to 1`: building or initiating something
- `turnaround`: improving a poor outcome or blocked situation
- `cognitive upgrade`: a moment that changed how the user thinks

For `largest challenge`, prefer `define -> decompose -> align/help -> result -> lesson`.

For `most memorable thing`, prefer `background -> action -> result/realization`.

### Reverse questions

Second-round reverse questions should show readiness for the role, not anxiety about personal benefits.

Better signals:
- `如果我加入，前 3 个月最需要优先补齐或承担的挑战是什么？`
- `团队现阶段最看重这个岗位的哪类能力？`
- `您觉得在这个团队里成长最快的人，通常做对了什么？`

Risky signals when asked too early:
- conversion timeline, salary, workload, or benefits questions without context

## Final-round / HR reverse-question model

Use this model when the user says `HR面反问`, `终面反问`, `问不出好问题`, or needs questions for HRBP, senior leader, or offer-stage conversations.

Good final-round reverse questions are not clever trivia. They reveal how the candidate evaluates fit and prepares to commit.

Build each question from:
- `what I already know`: one line based on JD, previous interview, or company research
- `what I need to judge`: success criteria, growth path, team reality, manager interface, or risk factor
- `why it matters`: how the answer helps the candidate do the role well
- `the question`: concise and non-defensive

High-signal question types:
- `success criteria`: `如果我加入，前三到六个月做到什么程度，您会认为这个人适配且值得继续培养？`
- `failure modes`: `以您观察，刚加入这个岗位的人最容易在哪类事情上卡住？是业务理解、协作节奏，还是优先级判断？`
- `culture in action`: `团队在目标很紧、资源有限时，通常怎么判断质量和速度的取舍？`
- `manager/team interface`: `这个岗位和 mentor/业务方的协作边界通常是怎样的？新人在哪些事情上应该主动推进，哪些需要及时同步？`
- `growth realism`: `在这个团队里，从合格到优秀的校招生/实习生，差距通常体现在哪些行为上？`
- `responsible commitment`: `为了让我对加入后的预期更准确，您觉得这个岗位最真实、也最需要提前适应的一面是什么？`

Risky final-round questions:
- `公司文化怎么样`
- `晋升空间大吗`
- `会不会加班`
- `多久能转正`
- `薪资还能不能谈`
- `您觉得我表现怎么样`

These topics are not forbidden, but they need framing. Safer framing:
- ask after role fit and success criteria first
- show why the information helps commitment or delivery
- avoid making benefits the only signal the interviewer hears
