---
name: xq-word
description: "Deep-dive English word mastery tool. Deconstructs a single English word into core semantics and epiphany. Use when user asks to explain/master a specific English word. Supports two modes: general vocabulary (default) and technical jargon (-t). Triggers on '解词', '单词', 'word', 'explain word'. For engineering terms like 'backpressure', 'throttle', 'coherency', 'virtualization', use '-t' flag for technical deep-dive."
version: "1.1.0"
user_invocable: true
---

## Usage

<example>
User: Deeply explain the word "Serendipity".
Assistant: [Calls xq-word with "Serendipity"]
</example>

<example>
User: /xq-word -t backpressure
Assistant: [Calls xq-word with "backpressure" in technical mode]
</example>

## Instructions

目标不是翻译，而是让用户掌握这个词的深层含义和用法。

### 模式

**默认模式**：通用英语词汇深度分析。

**技术术语模式 (`-t`)**：当用户指定 `-t` 或输入明显是工程黑话时，切换为技术术语专场模式。

### 默认模式输出结构

针对输入的 `word`（转换为小写，首字母大写），进行以下分析，直接在对话中用 Markdown 输出：

#### 1. 标题行

```
## {Word}  /{音标}/  {中文翻译}
```

#### 2. 核心语义

- **原始画面**: 用一句话描述该词源头最物理的画面（例如 Incubate: 母鸡趴在蛋上）。
- **核心意象**: 提炼公式（例如：温暖 + 时间 + 保护 = 孕育）。
- **解释**: 用充满洞见的语言阐述其深层含义与现代用法。分段清晰，**加粗**关键词。要有穿透力，展现词源、多领域含义之间的内在联系。

#### 3. 一语道破

一句中英双语的金句，必须具有哲学高度，总结该词的灵魂。用引用格式：

```
> "English sentence. 中文金句。"
```

### 技术术语模式 (`-t`) 输出结构

当用户指定 `-t` 时，输出改为工程师视角的深度拆解：

#### 1. 标题行

```
## {Word}  /{音标}/  {工程语境翻译}
```

#### 2. 精确语义

- **工程定义**: 一句话说出它在技术语境中的精确含义（不是词典释义）
- **核心机制**: 这个词描述的现象/机制是怎么运转的？数据/控制怎么流动？
- **常见误用**: 工程师最容易把这个词和什么混淆？误用的代价是什么？

#### 3. 语境地图

- **出现在哪**: 这个词在哪些系统/协议/框架中是最核心的概念？
- **邻居概念**: 和它最常一起出现的术语有哪些？它们之间的边界在哪？
- **反义词/替代词**: 什么时候不该用它？替代方案是什么？

#### 4. 可迁移性

- **跨域映射**: 这个概念从一个领域（如网络）迁移到另一个领域（如存储）时会怎么变形？
- **一句话精髓**: 用最少的字说出这个词在技术设计中的真正分量
