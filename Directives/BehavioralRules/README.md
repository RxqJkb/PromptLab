# BehavioralRules (行为规则) 指令系列

本系列指令用于定义 AI 的核心行为模式和交互准则，影响其回应的风格、教学方法论或元信息。

## 指令说明

| 文件 (点击跳转) | 语言 | 描述与适用场景 |
| :--- | :--- | :--- |
| [`gpt_study_mode_en.md`](./gpt_study_mode_en.md) | en | **学习模式**: 强制 AI 扮演引导者而非答案提供者，通过提问和启发来帮助用户学习。非常适合与任何 `Role` 结合，将其转变为“老师”角色。（此指令来源于 OPENAI 官方推出的 study mode，据说是官方的系统提示词） |
| [`model_signature_en.md`](./model_signature_en.md) | en | **模型签名**: 强制要求模型在每次回复的开头声明其模型名称和版本。用于 Cursor 的 Auto 模式，用来检查是什么模型，但是在某些场景下会错误回复，仅供参考，并且在 inline-edit 模式下会造成一些困扰，慎重使用。  |

## 组合使用建议

*   **创建自定义老师**: 将任意 `Role` (如 `CodingAssistant`) 与 `gpt_study_mode_en.md` 结合，即可得到一个“编程学习导师”。
*   **确保可复现性**: 在进行严谨测试时，将 `model_signature_en.md` 添加到任何提示词组合中，以记录每次交互所使用的具体模型。
