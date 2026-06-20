---
name: love-match
description: Analyze user personality traits through conversation or questionnaire, recommend compatible romantic partner types, provide detailed analysis for each match including reasons for compatibility, potential challenges, and relationship advice. Use when user asks about dating, relationships, personality compatibility, or relationship advice.
argument-hint: [mode: conversation|questionnaire]
disable-model-invocation: false
user-invocable: true
context: main
allowed-tools: []
---

# 恋爱匹配分析

当用户调用此技能时，执行以下步骤：

## 分析模式判断

根据 `$ARGUMENTS` 判断使用哪种模式：
- 如果参数包含 "questionnaire" 或 "问卷"，使用问卷模式
- 如果参数包含 "conversation" 或 "对话"，使用对话模式
- 默认使用对话模式

## 模式一：对话分析模式（默认）

如果使用对话模式，执行以下步骤：

1. **性格特征收集**
   通过开放式对话收集用户的性格信息。提出以下关键问题（每次只问2-3个，避免过载）：

   - "请描述你自己的性格特点，比如你是内向还是外向？"
   - "在亲密关系中，你最看重什么品质？"
   - "你平时喜欢什么样的活动和兴趣？"
   - "面对冲突时，你通常如何处理？"
   - "你理想中的恋爱关系是怎样的？"
   - "你有什么特别不能容忍的特质吗？"

   收集用户的回答，分析其性格特征，包括但不限于：
   - 社交倾向（内向/外向/平衡）
   - 情绪稳定性
   - 开放性程度
   - 责任心和可靠性
   - 价值观和生活态度
   - 沟通风格

2. **性格特征总结**
   在收集足够信息后，为用户总结其核心性格特征，使用结构化格式：
   ```
   你的性格画像：
   - 社交倾向：[描述]
   - 情绪特点：[描述]
   - 价值观：[描述]
   - 沟通风格：[描述]
   - 其他特征：[描述]
   ```

## 模式二：问卷分析模式

如果使用问卷模式，执行以下步骤：

1. **提供标准化问卷**
   为用户提供一组标准化问题，涵盖以下维度（每个维度2-3个问题）：

   **A. 社交倾向**
   - 在社交场合中，你通常感觉如何？
     a. 充满活力，享受结识新朋友
     b. 适度参与，喜欢小团体
     c. 偏好安静，更熟悉后才开放

   **B. 情绪管理**
   - 面对压力时，你通常如何应对？
     a. 寻求他人支持，主动沟通
     b. 自我消化，需要独处时间
     c. 混合方式，视情况而定

   **C. 价值观**
   - 在人生规划中，你目前最看重什么？
     a. 事业成就和个人成长
     b. 家庭幸福和稳定生活
     c. 探索体验和自由自在

   **D. 沟通风格**
   - 表达想法时，你更倾向于？
     a. 直接表达，不隐藏观点
     b. 温和委婉，考虑他人感受
     c. 视情况调整，平衡直接与委婉

   **E. 兴趣偏好**
   - 你更享受哪种类型的活动？
     a. 户外运动、冒险探索
     b. 艺术文化、深度交流
     c. 家中放松、安静时光

2. **分析问卷结果**
   根据用户的选择，总结其性格特征，格式同对话模式。

## 匹配推荐分析

基于用户的性格特征，推荐2-3种最匹配的恋爱对象类型，对每种类型提供详细分析：

### 推荐格式

**匹配类型 X：[类型名称]**

**为什么匹配**
- 解释该类型与用户性格的互补性和相似性
- 列举3-4个关键匹配点
- 使用具体场景说明如何契合

**潜在挑战**
- 列出2-3个可能遇到的问题或冲突点
- 说明这些问题可能如何表现
- 分析产生这些挑战的根本原因

**相处建议**
- 提供具体可行的建议（至少4条）
- 包括日常相处、冲突处理、共同成长等方面
- 每条建议都要具体、可操作

**注意事项**
- 提醒用户个性化差异的存在
- 建议在实际交往中持续观察和调整

## 持续学习和优化

1. **反馈收集**
   在完成分析后，询问用户：
   - "这个分析结果符合你的自我认知吗？"
   - "有什么需要补充或修正的地方吗？"
   - "你之前接触过类似类型的对象吗？感觉如何？"

2. **经验记录**（可选）
   如果用户愿意分享，记录：
   - 之前的恋爱经历
   - 与不同类型对象的相处体验
   - 成功或失败的案例

3. **优化建议**
   基于用户的反馈，调整分析结果，提供更个性化的建议

## 输出原则

- 使用简体中文，语言温和、客观、有同理心
- 避免绝对化的表述，使用"可能"、"通常"等限定词
- 鼓励用户将分析结果作为参考，而非绝对标准
- 强调真诚沟通和相互理解的重要性
- 保持积极正面的导向，帮助用户建立健康的恋爱观

## 特殊情况处理

- 如果用户提供的信息不足，主动引导补充关键信息
- 如果用户表现出负面情绪或心理困扰，提供适当的支持和建议，必要时建议寻求专业心理咨询
- 尊重用户的隐私，不主动追问敏感话题

---

**使用说明**：
- 调用方式：`/love-match` 或 `/love-match conversation` 使用对话模式
- 问卷模式：`/love-match questionnaire`
- 也可让 Codex 根据对话内容自动触发此技能

## References

- Read `references/questionnaire-design.md` when improving or explaining the assessment structure.
- Read `references/scoring-and-rules.md` when explaining dimensions, scoring, or insight rules.
- Read `references/report-framework.md` when writing or refining the final report format.
- Read `references/barnum-effect-avoidance.md` when checking whether the output is too generic.
