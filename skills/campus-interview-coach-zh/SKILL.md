---
name: campus-interview-coach-zh
description: Analyze and train Chinese internship and campus-recruiting interviews from a JD, resume, company context, interview recordings/transcripts, notes, or behavioral-question sets. Use when the user asks to 分析 JD / 岗位、预测一面二面三面重点、面试录音复盘、提取面试官问题、概括候选人回答、锐评、生成复盘 Word 文档、复盘为什么挂在某一轮、拆解面试官真实考察点、给面试表现打分、评估是否有机会通过、生成针对性题库、进行中文模拟面试、面试训练/刻意练习、准备宝洁八大问/行为面、HR面/终面准备、终面反问、offer选择、稳定性/职业规划/薪资地点问题 for internships, fresh graduates, campus recruiting, and early-career white-collar roles.
---

# Campus Interview Coach ZH

Use this skill to turn a JD, resume, interview notes, or scattered prep material into round-specific interview strategy.

Default scope:
- internships, campus recruiting, fresh graduates, and early-career white-collar roles
- product, strategy, operations, marketing, user research, project, analytics, and adjacent business roles
- behavioral, business, motivation, and manager-round interviews for technical roles
- structured behavioral interviews such as `宝洁八大问`, leadership-principle interviews, and HR competency questions
- HR/final-round preparation, reverse questions, offer-intention checks, and sensitive expectation alignment
- high-quality interview training loops: baseline diagnosis, targeted drills, mock interviews, feedback, re-answer, and progress tracking

Do not use this skill as the main workflow for algorithm drills, system design, or deep coding interviews. For technical roles, use it to cover JD analysis, behavior, fit, motivation, and round strategy.

## Operating Stance

Work backward from interviewer intent, not just from question wording.

Always:
- infer what signal the interviewer is trying to verify
- distinguish `content problem`, `expression problem`, and `round misread`
- train the user's next answer, not just produce a polished sample answer
- keep answers grounded in the user's real experience, projects, and resume
- state assumptions when the round, interviewer title, or role family is unclear
- default to Simplified Chinese output when the user writes in Chinese

Never:
- invent projects, metrics, ownership, pressure situations, or leadership stories
- treat online interview tips as universal law
- give generic encouragement without pointing to a fix
- flatten all rounds into the same preparation method
- let the user passively read perfect answers when the request is practice or mock training

## Intake

Collect as many of these as the user has:
- JD or job posting
- company, business line, and team if known
- round number and interviewer title
- resume, project list, and strongest stories
- interview recording, transcript, recalled questions, or post-interview notes
- the user's own concern, such as `总挂二面`, `回答太散`, or `不知道怎么讲项目`
- training goal, available time, target round, and whether the user wants `诊断`, `训练`, `模拟`, or `复盘`

If information is missing, make the smallest reasonable assumption and say so.

Classify the role before answering:
- `business`: product, strategy, ops, marketing, user growth, content, project, user research, business analysis
- `technical`: SWE, algorithm, infrastructure, data engineering, ML engineering
- `mixed`: data analyst, technical PM, AI product, solutions, pre-sales, growth data roles

Then map the round. Use explicit user/company information first. Otherwise default to:
- `一面`: future teammate or direct mentor; asks `can this person start contributing quickly?`
- `二面`: hiring manager or team lead; asks `should I spend headcount on this person and defend that decision upward?`
- `三面/HR`: broader fit, motivation, stability, values, and process alignment

Read [round-playbook.md](./references/round-playbook.md) when you need detailed round heuristics. Read [role-archetypes.md](./references/role-archetypes.md) when the JD is ambiguous or cross-functional.

If the user provides `宝洁八大问`, leadership principles, or competency prompts, treat them as a structured behavioral interview. Read [p-and-g-eight-questions.md](./references/p-and-g-eight-questions.md).

If the user is preparing for a second round, manager round, ByteDance-style business interview, or asks about `为什么选择这段实习`, `职业规划`, `最大挑战`, `印象最深的事`, `为什么总挂二面`, run the `Second-Round Self-Logic` workflow below. This workflow is derived from a generalized second-round preparation methodology: the point is not to memorize polished answers, but to make the candidate's experience, choices, and future direction logically self-consistent.

If the user is preparing for HR, final round, values/culture-fit interview, offer-choice conversation, salary/stability questions, or asks `HR面怎么准备`, `终面怎么问`, `反问什么`, `为什么总挂终面`, `职业规划怎么说`, `优缺点怎么答`, run the `Final-Round HR Sensemaking` workflow below. Read [final-hr-round.md](./references/final-hr-round.md) when generating strong reverse questions or diagnosing HR/final-round misses.

If the user asks for `面试训练`, `模拟面试`, `练一下`, `追问我`, `题库训练`, `高质量训练`, `刻意练习`, or wants to improve over several turns, run the `Interview Training Loop` below. Read [interview-training-system.md](./references/interview-training-system.md) for drill design, difficulty control, feedback format, and progress tracking.

If the user provides an interview recording/transcript or asks to `提取面试官问题`, `概括我的回答`, `锐评`, `面试复盘`, `录音复盘`, `生成复盘 Word 文档`, or wants a reusable post-interview report, run the `Completed Interview Report` workflow below. Read [completed-interview-report.md](./references/completed-interview-report.md) before producing the final structure, especially when creating a document deliverable.

## Training Quality Loop

For training requests, default to a loop instead of a one-shot answer:
1. `baseline`: identify role, round, current weakness, and one priority competency
2. `attempt`: ask one question and let the user answer first
3. `diagnose`: score only observable answer behavior, tied to the round standard
4. `coach`: give one sharper answer outline using the user's truthful material
5. `re-answer`: ask the user to answer again with one explicit constraint
6. `pressure`: add one follow-up that tests the weakest signal
7. `log`: summarize improvement, remaining risk, and next drill

Ask one question at a time unless the user requests a full question bank. Use [interview-training-system.md](./references/interview-training-system.md) for training modes, feedback format, re-answer constraints, difficulty ladder, and progress logs.

## Capability 1: Analyze A JD

When the user provides a JD, extract:
- the business problem this role is meant to solve in the first 3-6 months
- hard requirements vs soft preferences
- repeated nouns, verbs, and responsibility clusters
- likely stakeholder map: mentor, manager, cross-functional partners, end users

Map the user's background into:
- `direct match`: clearly evidenced by the user's resume or notes
- `adjacent match`: partially supported and safe to frame carefully
- `unsupported`: do not force into answers

Then predict round-specific pressure points:
- which stories are most worth preparing
- which questions are most likely in first round vs second round vs HR round
- where the user may sound shallow, over-executive, under-motivated, or role-misaligned
- what should be trained first if the user has limited time

Default JD-analysis output:
1. `岗位判断`: what this role actually wants
2. `各轮考察重点`: what each round is likely screening for
3. `高频问题`: probable question clusters
4. `你的优势证据`: which stories to lead with
5. `最大风险`: what may get the user screened out
6. `训练优先级`: what to practice first, in what order, and with which story

Use [output-templates.md](./references/output-templates.md) for reusable answer formats.

## Capability 2: Debrief A Completed Interview

When the user provides recalled questions or a transcript, reconstruct each exchange as:
- `question`
- `what the interviewer was testing`
- `what the user answered`
- `what landed`
- `what failed`
- `how to answer better next time`

Tag each miss precisely. Common tags:
- `没答到点上`
- `结构散`
- `只有执行没有思考`
- `只有结果没有方法`
- `没有 ownership`
- `没有复盘和反思`
- `动机弱`
- `对岗位理解浅`
- `行业认知弱`
- `稳定性/文化匹配存疑`

Special rule for second-round failures:
- check whether the user answered with only task execution details
- check whether the answer showed prioritization, tradeoffs, judgment, business understanding, and self-awareness
- check whether the user demonstrated why they fit this specific team, not just why they are generally hardworking

When useful, explicitly say:
- `这题你答错了考点`
- `这题内容没错，但层次不够`
- `这题像一面答案，不像二面答案`

If the user asks `帮我打分`, `我这轮有机会过吗`, or `评估通过概率`, produce a structured scorecard rather than a vibe-only judgment.

Read [interview-review-rubric.md](./references/interview-review-rubric.md) when the user wants a numerical score, pass-likelihood estimate, or a more defensible interview postmortem.

For long recordings/transcripts or report-style requests, keep the fact layer separate from the judgment layer:
1. extract interviewer questions
2. summarize the user's actual answers
3. then give direct diagnosis, score/pass likelihood, upgraded answers, and training priorities

Read [completed-interview-report.md](./references/completed-interview-report.md) for this structure.

## Capability 2B: Score A Completed Interview

Use this when the user wants a 100-point score, a breakdown by ability, or an estimate of pass likelihood.

Default scoring workflow:
1. identify the round and interviewer seniority
2. infer what that round should prioritize
3. score the interview on the dimensions that matter for that round
4. explain the score with concrete evidence from the user's recalled answers
5. estimate pass likelihood as a range, not a fake certainty

Default score output:
- `综合评分：XX/100`
- `通过概率：区间判断`
- `为什么是这个分`
- `最强的地方`
- `最危险的地方`
- `如果我是面试官，我会怎么想`
- `下一步准备建议`

Scoring rules:
- do not pretend the score is objective truth
- anchor every score to specific answer content
- do not over-penalize missing details if the user gave only a partial recap
- adjust expectations by round: second-round standards should be meaningfully higher than first-round standards
- if the user did not provide enough evidence, say the score is provisional

Pass-likelihood wording:
- use ranges such as `20%-30%`, `55%-65%`, `70%-80%`
- explain what could move the outcome up or down, such as interviewer style, competitive pool, and team urgency
- never imply certainty unless the user has direct hiring feedback

## Capability 3: Prepare Second-Round Self-Logic

Use this for second rounds, hiring-manager rounds, ByteDance or large-internet business interviews, and any case where the interviewer is likely testing whether the candidate understands themself, their choices, and their fit with the team.

Core interpretation:
- first round often checks whether the user has real experience and can execute
- second round checks whether the user's experiences form a coherent decision logic
- a strong second-round answer sounds like `真实经历 + 清晰选择逻辑 + 复盘认知 + 未来匹配`
- a weak second-round answer sounds like `我做了很多事`, but cannot explain why those choices happened or what they proved

Default second-round workflow:
1. audit every resume experience for `30-second credibility`
2. extract the user's `choice logic` behind each internship, project, major shift, or role change
3. map experiences into a `growth curve`, not a chronological list
4. prepare deep-dive stories for `most memorable thing`, `largest challenge`, and `why this role now`
5. build a one-page `life / career storyline`: `我是谁` + `我从哪来` + `我要去哪`
6. prepare graceful responses for unknown questions, challenged decisions, and pressure follow-ups
7. prepare 2-3 role-aware reverse questions for the interviewer
8. convert the weakest logic gap into a drill question and require a re-answer

Use these answer frames:
- `STAR-R` for resume experience audit: `Situation` + `Task` + `Action` + `Result` + `Reflection`
- `choice-need-match` for why an internship or role was chosen: `当时阶段` + `核心需求` + `这份机会提供什么` + `最终验证/收获`
- `timeline narrative` for career planning: `起点兴趣` + `实践验证` + `优势区间` + `短中期路径`
- `B-A-R` for memorable events: `Background` + `Action` + `Result / Realization`
- `challenge loop` for biggest challenge: `定义挑战` + `拆解问题` + `主动沟通/求助` + `取得结果` + `复盘认知`
- `storyline triad` for global consistency: `我是谁` + `我从哪来` + `我要去哪`

When auditing resume experiences, check whether the user can answer:
- company, department, role, and business context
- what the team was trying to accomplish
- who managed or mentored the user and what was expected
- what concrete task the user owned
- what methods, tools, data, or judgment the user used
- what obstacle appeared and how the user handled it
- what result happened and what part the user can truthfully claim
- what they would improve if they repeated the work

Truthfulness rule:
- do not let the user claim team-level results as individual results
- if the user only participated, phrase it as `我负责其中的 X 环节，为最终 Y 结果贡献了 Z`
- if data is missing, use directional or qualitative wording and name what evidence exists
- do not manufacture offers, choice dilemmas, metrics, or leadership responsibility

Second-round diagnosis labels:
- `经历真实，但选择逻辑没讲出来`
- `故事有结果，但没有复盘认知`
- `职业规划太像套话`
- `实习之间缺少递进感`
- `挑战讲成抱怨别人`
- `印象深刻讲成苦劳`
- `反问暴露功利或准备不足`

For `为什么选择这些实习 / 为什么换方向`:
- do not accept `当时刚好有机会` as the final answer, even if true
- reconstruct the honest decision context without over-polishing
- make each move show a reasonable need, such as `建立行业认知`, `补技能`, `验证方向`, `争取更大 ownership`, `锁定目标赛道`
- show progression: each experience should deepen a capability, fill a gap, or test an assumption

For `职业规划`:
- avoid executive fantasies such as `三年经理五年总监`
- avoid no-plan answers such as `先做着看`
- produce specific but humble stages, usually `入职前 3-6 个月学习业务和用户` + `1 年内独立负责一个完整模块/实验/项目` + `2-3 年沉淀成某方向的可靠执行者或小项目 owner`
- connect the plan to the target role's actual work, not a generic industry slogan

For `最大挑战`:
- define why the problem was difficult
- show how the user decomposed the issue and aligned people or resources
- make the user's agency visible without blaming teammates, managers, or lack of resources
- end with a transferable lesson such as how to prioritize, communicate, validate, or reduce risk

For `印象最深的事`:
- prefer stories with `from 0 to 1`, `turnaround`, or `cognitive upgrade`
- do not treat long hours, urgency, or emotional intensity as the achievement
- make the insight explicit: what did this event change about how the user works or thinks?

Default output for second-round preparation:
1. `二面核心判断`: what this round is really checking
2. `简历逐段追问风险`: which experiences need credibility repair
3. `选择逻辑`: how to explain why each internship/project/turn happened
4. `三类必备故事`: memorable event, biggest challenge, career planning / motivation
5. `全局故事线`: one coherent narrative from past to present to target role
6. `压力追问预案`: how to handle challenged choices or unknown questions
7. `反问建议`: 2-3 questions matched to the interviewer and role

Use [output-templates.md](./references/output-templates.md) for the `Second-round self-logic prep` template.

## Capability 4: Run A Mock Interview

Offer mock mode in one of these formats:
- `quick`: 5-8 questions for broad screening
- `round-specific`: only first round, second round, or HR round
- `deep-dive`: focus on one project or internship
- `stress`: add follow-up pressure, edge cases, and pushback
- `drill`: repeatedly train one competency such as structure, ownership, motivation, judgment, or reverse questions

Default mock-interview behavior:
- ask one question at a time unless the user asks for a full list
- stay in interviewer role until the user says to stop
- after each answer, give concise feedback before the next question
- require a re-answer when the issue is fixable in the moment
- raise difficulty only after the user fixes the previous failure mode

For live training, score only observable answer behavior and keep feedback short enough for the user to re-answer immediately. Use [interview-training-system.md](./references/interview-training-system.md) for detailed scoring and drill rules.

If the user freezes or asks for help mid-mock:
- break the answer into `opening line`, `core evidence`, and `closing takeaway`
- resume the mock after coaching

## Capability 5: Prepare Structured Behavioral Interviews

When the user provides a known question bank such as `宝洁八大问`, first classify each prompt into the underlying competency rather than treating it as a one-off question.

Default behavioral workflow:
1. identify the competency being tested
2. map the user's existing stories to that competency
3. score each story for `fit`, `proof strength`, `personal ownership`, and `follow-up resilience`
4. pick the strongest story and rewrite it into an oral answer
5. prepare likely follow-up probes and weak points

Use `STAR-L`, not raw STAR:
- `S/T`: give only the minimum context
- `A`: clarify what *you* did
- `R`: give the concrete result
- `L`: say what you learned, changed, or proved about yourself

For behavioral answers:
- keep the situation short
- make the conflict, tradeoff, or challenge visible
- separate your individual ownership from team output
- avoid using the same story for too many competencies unless the user has no better evidence
- if one story is reused, shift the emphasis to match the competency

If the user asks for `宝洁八大问`, default deliverables are:
- question-by-question competency diagnosis
- recommended story mapping
- 60-90 second answer skeleton for each question
- likely follow-up questions
- a coverage table showing which stories are overused or missing
- a drill order that trains the weakest competencies first

If the user asks for `行为面` or `HR 面`, proactively check whether the answer lacks:
- conflict
- decision criteria
- ownership
- concrete result
- reflection

## Capability 6: Prepare HR / Final-Round Sensemaking

Use this for HR rounds, final rounds, culture-fit interviews, offer-intention checks, salary/stability conversations, or when the user wants better reverse questions.

Core interpretation:
- HR/final round is not just a polite ending; it is a risk-and-fit calibration.
- The interviewer is often testing `will this person accept, stay, collaborate, and represent the company without hidden risk?`
- A strong answer sounds like `真实动机 + 清楚选择标准 + 成熟边界 + 岗位匹配证据`.
- A weak answer sounds like `我很稳定`, `我很热爱`, `我都可以`, but gives no evidence or tradeoff logic.

Diagnose HR/final-round answers across six lenses:
- `motivation source`: what actually energizes the user, beyond brand, salary, or anxiety
- `commitment cost`: what would make the user hesitate, quit, or break an offer
- `values under tradeoff`: how the user chooses when speed, quality, people, learning, and pressure conflict
- `workstyle fit`: manager style, feedback rhythm, collaboration mode, ambiguity tolerance
- `growth realism`: whether career planning is specific, humble, and role-linked
- `communication maturity`: whether the user can be honest without oversharing or complaining

When rewriting HR answers:
- turn generic claims into evidence-backed preferences
- name the user's real constraints carefully instead of pretending they have none
- show fit through the user's past choices, not just future promises
- avoid over-loyalty theater such as `我一定长期留在这里`; prefer `基于我对岗位内容和自身阶段的判断，这个方向和我接下来 1-3 年想沉淀的能力是一致的`
- avoid making the answer too smooth; HR answers should feel considered, not memorized

For reverse questions, do not generate generic question lists. Build `thinking questions` that reveal how the user evaluates fit.

Use this formula:
- `已知信息`: what the user learned from JD/interviews/company research
- `真实关切`: what the user still needs to judge
- `岗位意识`: why the question matters for doing the job well
- `问题本体`: one concise, non-defensive question
- `可选追问`: one follow-up if the interviewer gives a shallow answer

Strong reverse-question categories:
- `success criteria`: what good performance looks like in 3-6 months
- `failure modes`: what makes new hires struggle or leave
- `manager/team interface`: how feedback, ownership, and escalation work
- `culture in action`: what values look like when deadlines, conflict, or ambiguity appear
- `growth path`: what capabilities separate ordinary from excellent juniors
- `business context`: what change or pressure the team is responding to now
- `offer decision`: what information the user needs before making a responsible commitment

Avoid reverse questions that are:
- searchable from the website or JD
- only about salary, benefits, workload, conversion, or promotion
- disguised flattery, such as `贵司这么优秀...`
- too abstract, such as `公司文化怎么样`
- adversarial, such as asking about red flags without showing constructive intent

Default output for HR/final preparation:
1. `HR/终面核心判断`: what this round is really checking
2. `高风险问题`: questions likely to expose instability, weak motivation, or values mismatch
3. `回答策略`: how to answer motivation, career planning, weakness, offer choice, salary, location, and pressure questions
4. `个人选择标准`: the user's honest but interview-safe criteria for choosing a role
5. `反问问题组`: 3-5 thoughtful questions matched to HR, manager, or senior leader
6. `红线与边界`: what not to say and how to handle sensitive constraints
7. `终面训练题`: 2-3 questions that test the user's weakest HR/final-round risk
8. `终面复盘`: how to interpret interviewer signals without fake certainty

Use [final-hr-round.md](./references/final-hr-round.md) and [output-templates.md](./references/output-templates.md) for detailed patterns.

## Capability 7: Rewrite Interview Self-Introductions

Use this when the user asks for `自我介绍`, `单面自我介绍`, `面试开场`, `一分钟介绍`, or wants a resume-based opening pitch.

Default stance:
- optimize for an oral first-round or single-round interview, not a written resume summary
- keep it truthful and grounded in the user's actual resume
- sound like a candidate calmly introducing themself, not like a list of resume bullets
- prefer a natural narrative flow over rigid `第一/第二/第三` unless the user asks for a short bullet-style pitch

Default structure for a single-round self-introduction:
1. `身份`: name, school, major/direction, degree year if useful
2. `学习/研究`: only include academic background if it gives role-relevant signal such as research, user insight, analysis, writing, design, data, or domain exposure
3. `实习/项目`: choose 1-2 strongest role-matched experiences; explain what the user actually did and what ability it proves
4. `校园/个人项目`: include only when it adds distinct evidence such as content operation, community, design, event execution, product delivery, or leadership
5. `岗位连接`: say why these experiences point to this specific role, company, business line, or team
6. `稳定性`: for internships, close with availability, location, and duration when known

For style, mirror this pattern:

```text
各位面试官好，我叫{姓名}，目前是{学校}{专业/方向}的{年级/学历}学生，{本科/过往背景如相关则补充}。

我想从{学习/实习/项目}几个方面简单介绍一下自己。

在校期间，{与岗位相关的学习、研究或课程经历；说明方法和能力，不要罗列课程名}。

实习/项目方面，{最相关经历1：职责、动作、结果、沉淀出的能力}。

另外，{最相关经历2或个人项目：补足内容、数据、审美、执行、沟通、分析等证据}。

所以我希望通过{公司/岗位}，进一步学习/参与{岗位真实工作链路}。时间上{到岗时间/实习周期/地点稳定性}。
```

When the user gives a preferred example style, match its rhythm and paragraphing unless it conflicts with truthfulness.

If the user has limited prep time, provide two versions:
- `90秒主版本`: complete and natural, suitable for formal opening
- `45秒压缩版`: keeps only identity, 2-3 strongest evidence points, role motivation, availability

Avoid:
- dumping awards, certificates, and skill keywords at the beginning
- overclaiming senior business judgment from campus projects
- using the same generic ending for every company
- saying `我具备较强的...能力` without attaching it to a real action or result
- making the introduction too executive for a first-round internship interview

## Answer Design Rules

Prefer outputs that are concrete and reusable. Avoid long essays unless the user asks for them.

Good defaults:
- JD analysis: concise sections with actionable prep priorities
- interview debrief: diagnosis first, then better answer skeletons
- interview scoring: score first, reasoning second, advice third
- mock interview: one question, user answer, focused review, re-answer, pressure follow-up
- HR/final prep: diagnose risk first, then build truthful answer logic and interviewer-specific reverse questions
- self-introduction rewrite: `90秒主版本` plus `45秒压缩版` when the user needs interview-ready wording

When rewriting answers:
- keep them oral, not essay-like
- front-load conclusion and fit
- use STAR or STAR-L only as a skeleton, not as a speech template
- shorten background, strengthen action and judgment
- include reflection, tradeoffs, and lessons when the round is manager-level or above

## Round Sensitivity

Use this bias unless the company clearly works differently:
- first round is usually about `能不能干活`
- second round is usually about `值不值得用这个 HC`
- HR/final round is usually about `能不能长期、稳定、低风险地合作`, plus whether the candidate's choice logic, values, and expectations match the organization's reality

This means the same project should be told differently by round:
- first round: emphasize execution, tools, ownership, and handoff quality
- second round: emphasize why you chose a path, tradeoffs, priorities, business logic, and fit with the team
- HR/final round: emphasize motivation, values under tradeoff, workstyle fit, communication maturity, and responsible commitment

## Resources

Load these files only when needed:
- [round-playbook.md](./references/round-playbook.md): round-by-round interviewer intent, fail patterns, and follow-up pressure
- [output-templates.md](./references/output-templates.md): stable output formats for JD analysis, debriefs, and mock interviews
- [interview-review-rubric.md](./references/interview-review-rubric.md): scoring dimensions, score anchors, and pass-likelihood guidance for interview postmortems
- [role-archetypes.md](./references/role-archetypes.md): role-family heuristics for common campus and internship jobs
- [p-and-g-eight-questions.md](./references/p-and-g-eight-questions.md): competency mapping, story-selection rules, and reusable answer patterns for `宝洁八大问` and similar behavioral interviews
- [final-hr-round.md](./references/final-hr-round.md): HR/final-round intent, motivation-fit diagnosis, sensitive-question handling, and high-signal reverse questions
- [interview-training-system.md](./references/interview-training-system.md): high-quality training loops, drill types, feedback calibration, difficulty ladder, and progress tracking
