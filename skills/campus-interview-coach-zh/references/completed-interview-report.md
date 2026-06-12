# Completed Interview Report

Use this reference when the user provides an interview recording, transcript, recalled Q&A, or asks for a reusable `面试复盘`, `锐评`, `通过概率`, or Word/PDF-style report.

## Core Output Order

Default to this order unless the user asks otherwise:

1. `面试官问题提取`
2. `候选人回答概括`
3. `逐题锐评 / 复盘`
4. `综合评分与通过概率`
5. `高风险题升级版答法`
6. `训练清单 / 下次优先级`

Do not start with vague encouragement or an overall vibe. First reconstruct what happened.

## Audio Or Transcript Workflow

When the input is audio:
- transcribe first and preserve timestamps when feasible
- if the first transcription hallucinates or repeats prompt text, retry without an initial prompt and sample short clips before processing the full file
- mention uncertain proprietary names only when they affect interpretation; otherwise focus on question intent
- save transcript artifacts when working in a local workspace if useful

When the input is a transcript or recalled notes:
- group fragmented follow-ups under the same question
- distinguish interviewer question, candidate answer, and interviewer explanation
- keep a short evidence trail: quote or paraphrase only the answer material needed for diagnosis

## Fact Layer Before Judgment

Use a two-column or compact list:

| 面试官问题 | 候选人回答概括 |
| --- | --- |
| Q1 ... | ... |

For each question, capture:
- the actual question or normalized question
- the user's answer in one or two sentences
- the likely tested signal, if not obvious

This layer should feel factual, not evaluative.

## Diagnostic Layer

For each important question, diagnose:

```md
### Qx 题目
- 这题考什么：
- 你现在的回答：
- 锐评：
- 下一版怎么讲：
```

Use direct labels when accurate:
- `这题答错了考点`
- `这题内容没错，但层次不够`
- `这题像一面答案，不像二面/HR答案`
- `这是全场最强证据`
- `这是全场最大风险之一`

Common diagnostic buckets:
- `动机链不闭合`
- `职业规划虚`
- `岗位理解浅`
- `用户画像缺失`
- `只有方法，没有优先级`
- `项目真实，但个人决策边界不清`
- `没有逆境/犯错证据`
- `反问质量高但问法冒险`

## Scorecard

Use `interview-review-rubric.md` for score anchors. Adjust dimensions by round.

For HR/final-round reports, common dimensions:
- `表达与结构`
- `项目真实性`
- `ownership / 主动性`
- `岗位理解 / 动机匹配`
- `产品或行业理解`
- `成熟度与抗压`
- `抗追问能力`

Give a range for pass likelihood, not certainty. Explain the strongest positive signals and the main reasons it could still fail.

## Rewrite Layer

Give oral, reusable answers. Avoid perfect essay prose.

For each upgraded answer:
- start with the conclusion
- connect truthful past experience to target role
- include tradeoff, reflection, or next-step realism when the round is HR/manager-level
- do not invent metrics, offers, conflicts, or responsibilities

Default upgrade sections:
- `全局故事线`
- `职业规划`
- `为什么这个行业/岗位`
- `犯错/压力题`
- `陌生任务/紧急任务`
- `反问优化`

## Report-Style Deliverable

When the user asks for a Word document or reusable report, create a polished `.docx` using the Documents skill if available.

Recommended document structure:

```md
# 面试复盘报告

## 基本信息
- 复盘对象：
- 音频/文本来源：
- 复盘路径：
- 重要说明：

## 核心结论
- 一句话结论：
- 通过概率：

## 一、面试问题链路与回答概括
- A. 开场、职业规划与岗位选择
- B. 业务/行业/岗位理解
- C. 项目与协作深挖
- D. HR 风险校准：压力、性格、批评与计划
- E. 稳定性、选择标准与反问

## 二、关键锐评：这场到底卡在哪里
- 每个卡点包含：这题考什么 / 你现在的回答 / 锐评 / 下一版怎么讲

## 三、评分与通过概率
- 综合评分：
- 通过概率：
- 维度评分表：
- 如果我是面试官，我会怎么想：

## 四、下次可以直接使用的升级版回答
- 全局故事线
- 职业规划
- 为什么行业 / 岗位
- 犯错 / 压力题
- 陌生任务 / 时间紧任务

## 五、训练清单

## 六、下次面试的优先级
```

Design guidance for DOCX:
- serious internal brief style
- avoid huge prose walls; use tables only for true comparison/scoring
- use callouts for core conclusion and pass likelihood
- render and visually inspect the DOCX if document tooling is available

## Tone

The user asked for `锐评` means be direct, but still useful.

Good tone:
- `这题不是挂点，但会拉低确定性`
- `你不是能力不行，是选择逻辑没闭合`
- `这个故事是真强，但你没有把它前置成主证据`
- `这题要先回答考点，再补经历`

Avoid:
- personal attacks
- generic reassurance
- fake certainty about hiring outcome
- harshness without a replacement answer
