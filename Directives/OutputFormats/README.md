# OutputFormats (输出格式) 指令系列

本系列指令专注于规定 AI 回复内容的具体格式、布局和风格，以适应不同的下游应用（如笔记软件、文档生成等）。

## 指令说明

| 文件 (点击跳转) | 语言 | 描述与适用场景 |
| :--- | :--- | :--- |
| [`gemini_latex_zh.md`](./gemini_latex_zh.md) | zh | **LaTeX 数学公式格式**: 严格规定了行内公式 (`$..$`) 和独立公式 (`$$..$$`) 的使用规范，确保生成的数学内容格式标准。适用于需要撰写包含大量数学公式的科技文档或报告。（Gemini 的公式渲染问题常常在使用中造成大量错误显示，因此通过此提示词来进行规范约束，在测试中表现良好） |
| [`notion_zh.md`](./notion_zh.md) | zh | **Notion 笔记风格**: 要求 AI 使用 Notion 友好的 Markdown 语法进行回复，包括使用 Emoji、引用块、多级标题等元素来增强结构感和可读性。适用于需要将 AI 生成内容直接复制到 Notion 进行知识管理的场景。（一般适用于 Gemini 模型， GPT 系列特别是 4o 本身的输出风格就与 Notion 非常接近，无需特殊强调，可以使用提示词如“去除对话感”来规范即可得到满意的笔记内容） |

## 组合使用建议

*   **撰写科研笔记**: `Roles/PaperReadingAssistant/v1_zh.md` + `gemini_latex_zh.md` + `notion_zh.md`。这个组合可以让 AI 在解答论文问题时，以 Notion 风格输出包含标准 LaTeX 公式的高质量笔记。
*   **生成带码块的教程**: `Roles/CodingAssistant/base_v2_zh.md` + `notion_zh.md`。
