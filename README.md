# 深度研究 / Deep-Research

> **Tick 阶段的认知基础设施。不是帮你写更多代码，是帮你建立不写代码也能掌控系统的底气。**

---

## 核心洞察

AI 时代的工程产出遵循一个非线性方程：

```
有效架构价值 = AI 杠杆收益 × ln(1 + D_base) − 认知债务惩罚 × e^(A − D_base)
```

- **A**（抽象层级）：AI 能帮你把系统建得多高、多复杂
- **D_base**（底层基石）：不依赖 AI，你自己对机制层的真实掌控度

**关键结论**：当 **A > D_base** 时，认知债务呈**指数爆炸**。你感觉到的"虚幻感""不真实感""系统失控"——不是情绪，是数学。系统在客观上运行良好，但在你的主观认知中是一个黑盒。这种理解偏差的累积，是复杂系统未来不可维护的根本原因。

**Tick-Tock 范式**是解：
- **Tock**：拥抱 AI，拉升 A，快速构建上层架构（AI 已经做得很好了，不需要这套 skills）
- **Tick**：深潜降维，禁用 AI，亲手触碰底层，提升 D_base（**这套 skills 只为这个阶段服务**）

---

## 为什么全是"学习/研究"技能？

因为代码生成是 Tock 阶段的事，AI 已经比你快十倍。真正稀缺的是 **D_base**——看到一个新概念时，能把它安放进已有认知结构的效率和深度。

D_base 不是知识量。是你读完一篇论文，带走的是**方法论**还是**名词和数字**；是你面对一个 Bug，能**降维到机制层排查**还是只能**盲调参数**；是你评估一个新技术，能判断它**在创造新秩序还是搬运旧方案**。

这套 skills 不做知识搬运。它做三件事：

1. **解剖** — 把新概念拆到机制层（xq-learn）
2. **降秩** — 把复杂领域砍到不可再少的生成器（xq-rank）
3. **评估** — 用统一框架判断新技术值不值得投入学习（xq-invest）

其余技能是这三件事的延伸：读论文是为了提取思路基因（xq-paper），写博客是为了在写的过程中想透（xq-writes），白话是为了验证自己真懂了（xq-plain），性能调优是为了建立系统级直觉（xq-perf），技术评审是为了暴露盲区（xq-roundtable），铸卡是为了把认知成果固化成可传播的形态（xq-card）。

**每个 skill 都是 Tick 阶段的一个认知原子**——原子化、可组合、可复用，像设计系统模块一样设计自己的学习过程。

---

## Quick Install

```bash
git clone https://github.com/Qiang-Xuu/Deep-Research.git ~/.claude/skills/Deep-Research && echo "Restart Claude Code to load skills"
```

Or step by step:

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/Qiang-Xuu/Deep-Research.git ~/.claude/skills/Deep-Research

# (Optional) Install xq-card dependencies for PNG card generation
cd ~/.claude/skills/Deep-Research && bash scripts/install.sh

# Restart Claude Code
```

**Requirements**: None for most skills. `xq-card` requires [Node.js](https://nodejs.org/) + Playwright.

---

## Skills: Tick 阶段的认知原子

### Core — D_base 建设

| Skill | Tick 作用 | What it does |
|-------|-----------|--------------|
| **xq-learn** | 解剖概念到机制层 | 8 维解剖：历史、机制、边界、对比、代价、实践、美感、元反思。把一个技术概念拆到你能用它解释其他东西的程度。 |
| **xq-rank** | 降秩到不可再少的生成器 | 给一个领域，找出真正独立的生成器有几个。用它们能反向生成全部现象？能，才算找到。建立的是**结构化直觉**。 |
| **xq-invest** | 判断值不值得投入学习 | 用"秩序创造机器"框架评估新技术：飞轮在不在转？冲击后变强还是变弱？资源是推过来的还是自己来的？避免为搬运旧方案的技术浪费时间。 |

### Input — 知识摄入

| Skill | Tick 作用 | What it does |
|-------|-----------|--------------|
| **xq-paper** | 读论文提取思路基因 | 不为复制代码，为**思路考古**（这个解法被什么真问题逼出来的？）、**方法论提取**（这个思路能嫁接到我系统的哪一块？）、**迁移试探**（嫁接需要什么条件？）。 |
| **xq-word** | 掌握技术术语的精确语义 | 默认通用词 + `-t` 技术术语模式。拆解工程黑话（backpressure, throttle, coherency）的精确机制、常见误用、跨域可迁移性。**术语不精确，思考就不精确。** |

### Process — 想透与验证

| Skill | Tick 作用 | What it does |
|-------|-----------|--------------|
| **xq-writes** | 在写的过程中想透 | 带着一个技术观点出发，找核→攻核→找类比→展开→磨。输出技术博客/散文。**写不清楚就是没想清楚。** |
| **xq-plain** | 验证自己真懂了 | 把技术内容改写到跨团队也能懂，但**附带精确证据**（数据、条件、边界）。能用大白话讲清楚，才算真懂。 |
| **xq-perf** | 建立系统级直觉 | 输入性能症状→输出假设树→验证实验（按成本排序）→根因确认→优化方向。**性能调优的本质是建立"系统如何在物理层运转"的直觉。** |
| **xq-roundtable** | 暴露盲区 | 多工程角色（性能、安全、架构、可靠性）围绕一个设计决策辩论。你不是在听答案，是在看**自己没考虑到的维度**。 |

### Output — 认知固化

| Skill | Tick 作用 | What it does |
|-------|-----------|--------------|
| **xq-card** | 把认知成果铸成可传播形态 | 内容→PNG 视觉卡片。技术博客风：信息密度优先、代码友好、深色主题。铸的是**思想**，不是排版。 |

### Meta

| Skill | What it does |
|-------|--------------|
| **xq-skill-map** | 扫描所有已安装技能，渲染 ASCII 概览 |

---

## Workflows

| Workflow | Chain | What it does |
|----------|-------|--------------|
| **xq-paper-flow** | xq-paper → xq-card | 读论文 + 铸卡。输入论文，输出分析 org + 阅读卡 PNG。读的时候在想，铸的时候在想得更清楚。 |
| **xq-word-flow** | xq-word → xq-card -i | 解词 + 铸信息图。把一个技术术语的精确语义可视化。 |

---

## Usage Examples

```
# Tick: 解剖一个核心概念到机制层
/xq-learn PCIe SR-IOV

# Tick: 给一个领域降秩，找不可再少的生成器
/xq-rank 分布式推理系统的通信瓶颈

# Tick: 读论文提取思路基因和方法论
/xq-paper https://arxiv.org/abs/2401.12345

# Tick: 评估一项新技术值不值得投入学习
/xq-invest eBPF

# Tick: 性能症状→系统化根因排查
/xq-perf 服务P99延迟从5ms涨到50ms，CPU没满，内存正常

# Tick: 暴露设计盲区
/xq-roundtable 我们的推理服务应该坚持同步API还是改为异步队列？

# Tick: 验证自己真懂了
/xq-plain 用大白话解释NUMA架构对延迟的影响，附带具体数字

# Tick: 掌握一个技术术语的精确语义
/xq-word -t backpressure

# Tick: 把想透的观点铸成可传播形态
/xq-card -i 输入：关于PCIe带宽争抢的分析结论...
```

---

## 设计哲学

### 原子化
每个 skill 只做一件事。像系统模块一样——单一职责、清晰接口、可组合。

### 触底
每个解释必须到达机制层。"它像魔法一样工作"是不可接受的。Tick 阶段的唯一标准：**你能不能用这个知识解释另一个现象**？

### 证据优先
每个判断附带数据、条件、边界。工程师的严谨不能为易懂让路。

### D_base > A 原则
这套 skills 不会帮你生成更多代码（那是 Tock 阶段的事）。它只回答一个问题：**你的 D_base 够不够支撑你正在用 AI 构建的抽象层级？**

---

## 与 EAV 理论的关系

这套 skills 是 **EAV（有效架构价值）方程** 和 **Tick-Tock 范式** 的工程化落地。

- **EAV 方程**告诉你：为什么盲目用 AI 拉升 A 会导致认知债务指数爆炸
- **Tick-Tock 范式**告诉你：什么时候该禁用 AI 深潜底层，什么时候该拥抱 AI 快速构建
- **Deep-Research skills**告诉你：深潜的时候，怎么最高效地提升 D_base

**不是反对 AI。是反对在 D_base 不足的情况下滥用 AI。**

---

## Development

### Add a New Skill

```bash
cp -r skills/xq-rank skills/xq-your-skill
# Edit SKILL.md with YAML frontmatter + instructions
```

### File Conventions

- **Org-mode output**: `*bold*` (single asterisk), filenames `{timestamp}--{title}__{type}.org`, directory `~/Documents/notes/`
- **ASCII art**: Only `+ - | / \ > < v ^ * = ~ . : # [ ] ( ) _ , ; ! ' "` and spaces
- **Timestamps**: `date +%Y%m%dT%H%M%S`

---

## License

MIT

---

**Maintainer**: [qiangxu](https://github.com/Qiang-Xuu)  
**Context**: Embedded systems, autonomous driving, HPC, distributed inference, PCIe, virtualization, performance tuning.
