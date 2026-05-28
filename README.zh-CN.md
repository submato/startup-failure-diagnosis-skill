# Startup Failure Diagnosis Skill 中文版

一个用于**创业失败诊断、创业想法验证、PMF 风险分析、CAC/LTV 判断、单位经济模型审查、创业项目 kill criteria 设计**的开源 Agent Skill。

English: [README.md](README.md)

这个 skill 从 **1100+ 个失败创业案例**中提炼常见死亡模式，并结合 Loot Drop 公开的创业失败研究，把“创业建议”变成一套可执行的诊断流程。

它不是泛泛地说“你要验证市场”，而是帮你回答：

```text
这个创业想法最可能怎么死？
哪些风险最先杀死项目？
什么证据可以证明这个判断是错的？
7-14 天内应该做什么验证？
达到什么条件就应该停止或转向？
```

## GitHub SEO Keywords

`创业失败诊断`, `创业想法验证`, `PMF 风险`, `产品市场匹配`, `商业模式诊断`, `CAC LTV`, `单位经济模型`, `创业尸检`, `失败创业案例`, `独立开发者工具`, `Cursor skill`, `Agent skill`, `startup failure diagnosis`, `startup idea validation`, `startup autopsy`

## 它能做什么

- 将创业想法映射到常见失败反模式。
- 从需求、产品、竞争、分发、单位经济模型、现金流、运营、监管、团队等维度打分。
- 输出最可能的失败链条。
- 找出 3 个最危险的 red flags。
- 反推需要哪些证据才能降低风险。
- 设计 7-14 天内能执行的验证实验。
- 设置明确的 stop / pivot / continue 标准。
- 如果需求仍然成立，给出更安全的 rebuild angle。

## 为什么要做这个 Skill

很多创业分析太空泛：

```text
验证市场
关注用户需求
控制成本
做好差异化
```

这些建议没错，但不够具体。

这个 skill 的目标是把 1100+ 个失败创业案例里反复出现的模式，压缩成一套“创业项目前置尸检”流程。你可以在写代码、招人、投广告、融资之前，先判断这个项目最可能死在哪里。

## 适合谁用

- 正在验证创业想法的 founder。
- 准备做 MVP 的 indie hacker。
- 想判断项目是否值得继续投入的独立开发者。
- 审查新产品方向的产品经理。
- 想做 startup pre-mortem 的投资人。
- 想把失败创业案例重新包装成新机会的 builder。

## 安装方式

把 skill 文件夹复制到项目内：

```bash
.agents/skills/startup-failure-diagnosis/
```

或者作为个人 skill 安装：

```bash
~/.cursor/skills/startup-failure-diagnosis/
```

核心文件：

```text
startup-failure-diagnosis/SKILL.md
```

辅助文件：

```text
startup-failure-diagnosis/antipatterns.md
startup-failure-diagnosis/examples.md
```

## 快速使用 Prompt

```text
Use the startup-failure-diagnosis skill to evaluate this idea:

[填写你的创业想法]

Return:
1. One-line verdict
2. Most likely failure chain
3. Risk scorecard from 0-5
4. Red flags
5. Counter-evidence needed
6. 7-14 day validation plan
7. Kill criteria
8. Rebuild angle
```

中文也可以这样问：

```text
请使用 startup-failure-diagnosis skill 分析这个创业想法：

[填写你的创业想法]

要求输出：
1. 一句话判断
2. 最可能的失败链条
3. 0-5 分风险评分
4. 关键 red flags
5. 需要哪些反证
6. 7-14 天验证计划
7. kill criteria
8. 如果继续做，应该怎么重构切入点
```

## 示例

输入：

```text
我想把这个 skill 开源，然后做一个线上版本收费。首次免费，后续按次收费。
```

输出风格：

```text
一句话判断：
高风险，除非开源 skill 被当作分发入口，而付费产品卖的是“决策级创业诊断报告”，不是简单调用一次 AI。

最可能失败链条：
No Market Need -> Distribution Vacuum -> Competition / Commodity Trap -> Unit Economics

核心红旗：
如果用户可以复制开源 skill 在本地直接使用，线上付费版必须提供比“调用一次 AI”更强的价值边界。
```

完整 demo 见：[demos/conversation-5a314bdf.md](demos/conversation-5a314bdf.md)

## 诊断输出格式

```markdown
## One-Line Verdict
[一句话判断 + 信心等级]

## Most Likely Failure Chain
[反模式 A] -> [反模式 B] -> [反模式 C]

## Risk Scorecard
- Demand: [0-5] - [原因]
- Product/Tech: [0-5] - [原因]
- Competition: [0-5] - [原因]
- Distribution: [0-5] - [原因]
- Unit Economics: [0-5] - [原因]
- Cash/Runway: [0-5] - [原因]
- Operations/Regulation/Team: [0-5] - [原因]

## Red Flags
- [具体风险]

## Counter-Evidence Needed
- [什么证据能降低这个风险]

## 7-14 Day Validation Plan
1. [验证实验]

## Kill Criteria
- 如果 [指标阈值] 在 [时间/样本量] 内达不到，就停止或转向。

## Rebuild Angle
[如何缩小人群、改变渠道、优化成本、建立防御性]
```

## 核心失败反模式

这个 skill 会重点检查：

- No Market Need：用户觉得有意思，但不愿付费或迁移。
- Ran Out of Cash：到收入出现前，现金流先死。
- Team/Founder Conflict：团队能力、目标或决策权冲突。
- Competition：被平台、大公司或同类产品复制、捆绑、碾压。
- Product/Tech Failure：demo 能跑，但真实场景不稳定、不可信、不好用。
- Legal/Regulatory Issues：监管、合规、数据、责任边界挡住落地。
- Unit Economics：增长越快亏越多。
- Distribution Vacuum：产品做好了，但没有可重复获客渠道。
- Operational Scalability Trap：看起来是软件，实际靠人力、运营、物流或人工服务堆出来。
- AI-Specific Commodity Trap：只是 AI wrapper，没有数据、工作流或分发护城河。

## 免责声明

这个 skill 提供商业分析，不构成投资、法律或财务建议。请用真实客户、付费意愿、留存数据、单位经济模型和必要的法律意见验证结论。

## License

Apache-2.0.
