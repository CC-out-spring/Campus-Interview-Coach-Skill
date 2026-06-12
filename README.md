<div align="center">

# Interview Coach Skill

### 面试完回听录音，才知道自己刚才在说什么。

**一个中文校招 / 实习面试复盘、JD 辅导、模拟追问 Skill。**

<br />

<img src="./skills/campus-interview-coach-zh/image" width="520" />

<br />
<br />

![Interview](https://img.shields.io/badge/Interview-Coach-blue)
![Language](https://img.shields.io/badge/Language-中文-red)
![Campus](https://img.shields.io/badge/Scope-校招%20%7C%20实习%20%7C%20Early--career-green)
![No Fabrication](https://img.shields.io/badge/原则-不编经历-black)

[这是什么东西](#这是什么东西) · [谁适合用](#谁适合用) · [怎么用](#怎么用) · [它会干嘛](#它会干嘛) · [项目结构](#项目结构)

</div>

---

## 这是什么东西

这是一个中文面试 Coach Skill。

一开始是给我自己用的。

面试的时候感觉自己答得还行，回去一听录音，发现自己不是在回答问题，是在给面试官做一场没有目录的个人经历朗诵。

普通 AI 复盘也很礼貌：

```text
整体表达较流畅，但建议进一步增强结构化表达，
突出岗位匹配度，体现个人思考。
```

没错。

但我下次还是不知道自己到底死在哪。

所以有了这个 Skill。

它主要做三件事：

```text
面前：结合简历 + JD，判断这轮到底该讲什么。
面后：结合录音 / 问题回忆，拆每题到底在考什么。
训练：先让你答，再拆你，再让你重答，再追问。
```

不是面试答案生成器。

更像一个不太会安慰人的复盘搭子。

---

## 谁适合用

适合这些场景：

- 实习面试
- 校招面试
- 暑期实习
- 产品 / 运营 / 策略 / 市场 / 用户研究 / 商分等商业岗
- AI 产品、技术 PM、数据分析等 mixed 岗
- 行为面、HR 面、终面、宝洁八大问
- 面完有录音、转写、问题回忆，想知道自己到底哪里没答好
- 面前有简历和 JD，想提前准备追问
- 一面过，二面老挂
- HR 面总觉得自己答得很标准，但很没记忆点

尤其适合这种状态：

```text
我知道我做过项目。
但我不知道面试官到底想听哪部分。

我知道我回答了。
但我不知道我有没有答到点。

我知道 AI 说得都对。
但它说完以后我还是不会改。
```

---

## 怎么用

打开：

```text
skills/campus-interview-coach-zh/SKILL.md
```

把全文复制 / 上传 / 丢给支持长上下文的 AI。

然后按你的场景补 prompt。

### 面试后复盘

```text
请严格按照这份 Campus Interview Coach Skill 执行。
下面是我的面试录音转写 / 问题回忆。
请逐题复盘：面试官真正想看什么、我答到了没有、哪里像流水账、
哪里需要补判断或取舍，并给出下次更好的答法骨架。
```

### 面前准备

```text
请严格按照这份 Campus Interview Coach Skill 执行。
下面是我的简历和目标 JD。
请判断这个岗位真正想招什么人、各轮可能考察什么、
哪些经历最值得讲、哪些地方容易被追问，并给我一轮模拟面试训练。
```

### 二面 / 主管面

```text
请严格按照这份 Campus Interview Coach Skill 执行。
我在准备二面 / 主管面。
请重点帮我检查：经历选择逻辑、项目判断、取舍、业务理解、岗位匹配，
不要只生成标准答案，要先追问我。
```

### HR / 终面

```text
请严格按照这份 Campus Interview Coach Skill 执行。
我在准备 HR 面 / 终面。
请帮我准备动机、稳定性、职业规划、offer 选择、薪资地点等敏感问题，
并给出高质量反问。
```

---

## 它会干嘛

它会尽量帮你：

- 拆 JD，判断岗位真实需求
- 区分一面、二面、HR / 终面的考点
- 复盘面试录音或问题回忆
- 判断每题是内容问题、表达问题，还是轮次误读
- 给通过概率和评分，但不装算命
- 训练自我介绍、项目深挖、行为面、HR 面
- 根据简历和 JD 预测追问
- 做模拟面试：先答、再拆、再重答、再追问
- 帮你设计终面 / HR 面的反问

它不会帮你：

- 编经历
- 编数据
- 把参与写成主导
- 把校园项目写成商业传奇
- 把每个答案都腌成“结构化表达 + 岗位匹配度”
- 一上来就端一盘漂亮但不像人的标准答案

它的核心原则：

```text
不编。
不飘。
不硬装。
先判断面试官到底在问什么。
再训练你下一次怎么答。
```

---

## 项目结构

```text
Campus-Interview-Coach-Skill/
└── skills/
    └── campus-interview-coach-zh/
        ├── SKILL.md
        ├── image
        ├── agents/
        │   └── openai.yaml
        └── references/
            ├── completed-interview-report.md
            ├── final-hr-round.md
            ├── interview-review-rubric.md
            ├── interview-training-system.md
            ├── output-templates.md
            ├── p-and-g-eight-questions.md
            ├── role-archetypes.md
            └── round-playbook.md
```

---

## 作者

小红书：`Spring_wall`

欢迎交流面试复盘、校招准备、AI 工作流和各种求职精神状态。

---

<div align="center">

**Oren Campus Interview Coach Skill**

面试已经够玄了。  
复盘的时候，至少让我知道自己到底死在哪。

</div>
