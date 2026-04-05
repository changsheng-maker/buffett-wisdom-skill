# buffett-wisdom

**Warren Buffett Investment Wisdom Assistant for Claude Code**

Transforms Claude into a Buffett-level investment thinking partner, drawing from the complete collection of 98 Buffett letters stored in the user's Obsidian vault.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Claude Code Compatible](https://img.shields.io/badge/Claude%20Code-Compatible-green.svg)](https://claude.ai/code)

---

## Table of Contents

- [Installation](#installation)
- [What It Does](#what-it-does)
- [How It Works](#how-it-works)
- [Usage Examples](#usage-examples)
- [Vault Structure](#vault-structure)
- [Trigger Keywords](#trigger-keywords)
- [Data Sources](#data-sources)
- [Evaluation Results](#evaluation-results)
- [Contributing](#contributing)

---

## Installation

### Method 1: Drag and Drop (Easiest)

1. Download the `buffett-wisdom.skill` file from this repository
2. Open Claude Code
3. Drag the `.skill` file into the Claude Code window
4. The skill will be automatically installed and ready to use

### Method 2: Manual Installation

```bash
# Clone repository
git clone https://github.com/changsheng-maker/buffett-wisdom-skill.git

# macOS
cp buffett-wisdom-skill/buffett-wisdom.skill ~/.claude/skills/

# Linux
cp buffett-wisdom-skill/buffett-wisdom.skill ~/.claude/skills/

# Windows — copy to %USERPROFILE%\.claude\skills\
```

### Method 3: Development Mode (Symlink)

```bash
ln -s /path/to/buffett-wisdom-skill/buffett-wisdom.skill ~/.claude/skills/buffett-wisdom.skill
```

---

## What It Does

Transforms Claude into a Warren Buffett investment expert by searching your personal Obsidian vault containing the complete collection of Buffett's writings.

### Core Features

| Feature | Description |
|---|---|
| **Concept Explanations** | Deep explanations of Buffett concepts (护城河/安全边际/内在价值/市场先生/能力圈) with exact quotes |
| **Quote Search** | Find Buffett's exact words across 98+ letters (1965-2024) |
| **Company Analysis** | Analyze companies through Buffett's investment framework (61 companies documented) |
| **Philosophy Application** | Apply Buffett's thinking to modern investment decisions |
| **Historical Context** | Track how Buffett's views evolved across four eras (1956-present) |
| **Cross-Reference** | Connect concepts, companies, and letters through rich bidirectional linking |

### Supported Trigger Types

- **Concept questions**: "什么是护城河", "Explain margin of safety"
- **Philosophy questions**: "巴菲特怎么看市场波动", "Why long-term holding matters"
- **Company questions**: "巴菲特为什么投苹果", "What's special about GEICO"
- **Historical questions**: "1987股灾巴菲特做了什么", "How did Buffett meet Munger"
- **Application questions**: "用巴菲特的框架分析X公司", "How would Buffett analyze this"
- **Quote questions**: "巴菲特说过什么关于护城河", "Quote about Mr. Market"

---

## How It Works

The skill searches your Obsidian vault at `~/Documents/Obsidian/花海/04 Knowledge 知识网络/05 Topics 专题领域/09 巴菲特投资/`

### Answering Strategy

1. **Identify question type** — concept, quote, company, philosophy application, or historical
2. **Targeted search** — read the relevant concept card first, then find supporting letters/companies
3. **Synthesize** — build answer from:
   - Concept definition (in Buffett's own words)
   - 2-3 powerful quotes
   - Canonical examples (GEICO, Coca-Cola, Washington Post)
   - Evolution across eras
   - Related concept links

### Response Style

1. **Lead with conclusion** — one sentence answering the core question
2. **Use Buffett's exact words** — cite him directly
3. **Concrete data** — investment years, returns, multiples
4. **Non-obvious insight** — what do most people miss?
5. **End with action** — what should the user think or do next?
6. **Cite the vault** — reference the source file for further reading

---

## Usage Examples

### Example 1: Moat Concept

**Prompt:**
```
解释巴菲特的"护城河"概念，用他的话和实际案例说明
```

**What the skill does:**
- Reads `concepts/护城河.md`
- Finds the 2007 letter quote about durable moats
- Identifies two types: low-cost (GEICO) and strong brand (Coca-Cola)
- Pulls specific investment return data

**Expected output:**
> "护城河是巴菲特最核心的投资概念之一。2007年他在股东信中说：'一道需要不断重建的护城河，其实根本没有护城河。'他将护城河分为两种类型：低成本优势（如GEICO保险）和强品牌（如可口可乐）。GEICO的市场份额从2.5%增长到12%，正是护城河威力的证明。"
> — [[2007-巴菲特致股东信]]

---

### Example 2: Mr. Market

**Prompt:**
```
巴菲特怎么看市场波动？市场先生这个比喻是什么意思？
```

**What the skill does:**
- Reads `concepts/市场先生.md`
- Finds the 1987 letter quote about market being a servant not a guide
- Explains how volatility creates opportunity
- Gives the 1973 Washington Post example

**Expected output:**
> "市场先生来自格雷厄姆的《聪明的投资者》，不是巴菲特的发明，但巴菲特最爱用这个比喻。他说：'市场先生是来为你服务的，不是来引导你的。对你有用的是他的钱包，而不是他的智慧。'1973年华盛顿邮报大跌时，巴菲特看透了市场先生的情绪，反而大举买入。"
> — [[1987-巴菲特致股东信]]

---

### Example 3: Apple Investment

**Prompt:**
```
巴菲特投资苹果的逻辑是什么？从他的股东信里找依据
```

**What the skill does:**
- Reads `companies/苹果.md`
- Cross-references with `concepts/护城河.md`
- Finds specific Apple quotes from Berkshire letters
- Analyzes brand loyalty and ecosystem as moat components

**Expected output:**
> "巴菲特投资苹果的核心逻辑是护城河。他看中的是苹果生态系统的忠诚度——用户一旦进入苹果生态，转换成本极高。2018年他在股东信中提到：'苹果产品的受欢迎程度令人难以置信，特别是对用户粘性的贡献。'这不是普通消费品的护城河，而是生态系统的护城河。"
> — [[2018-巴菲特致股东信]]

---

### Example 4: Quote Extraction

**Prompt:**
```
巴菲特关于"安全边际"说过的最经典的话是什么？
```

**What the skill does:**
- Reads `concepts/安全边际.md`
- Finds the most powerful safety margin quotes
- Contextualizes when and why he said them

---

### Example 5: 1987 Crash

**Prompt:**
```
1987年股灾时巴菲特做了什么？他怎么应对的？
```

**What the skill does:**
- Reads `berkshire/1987-巴菲特致股东信.md`
- Finds relevant sections on market crash response
- Explains his philosophical approach to volatility

---

### Example 6: Munger's Influence

**Prompt:**
```
巴菲特和芒格是什么关系？芒格如何影响巴菲特的投资哲学？
```

**What the skill does:**
- Reads `people/芒格.md`
- Traces the intellectual relationship
- Explains the shift from Graham-ism to quality-at-reasonable-price

---

## Vault Structure

The skill draws from the 花海 Obsidian vault at `~/Documents/Obsidian/花海/04 Knowledge 知识网络/05 Topics 专题领域/09 巴菲特投资/`

```
09 巴菲特投资/
├── concepts/          # 49 concept cards
│   ├── 内在价值.md    # Intrinsic value
│   ├── 护城河.md      # Moat / competitive advantage
│   ├── 安全边际.md    # Margin of safety
│   ├── 市场先生.md    # Mr. Market
│   ├── 能力圈.md     # Circle of competence
│   ├── 保险浮存金.md # Insurance float
│   └── ...           # 40+ more concepts
├── companies/         # 61 company analyses
│   ├── 苹果.md        # Apple
│   ├── 盖可保险.md    # GEICO
│   ├── 可口可乐.md    # Coca-Cola
│   └── ...           # 56 more companies
├── people/            # 7 key figures
│   ├── 芒格.md        # Charlie Munger
│   ├── 格雷厄姆.md    # Ben Graham
│   └── ...
├── berkshire/         # 60 Berkshire shareholder letters (1965-2024)
├── partnership/       # 35 partnership letters (1956-1970)
└── special/          # 3 special letters
```

### Vault Statistics

| Category | Count | Content |
|---|---|---|
| Concept Cards | 49 | Core investment concepts |
| Company Analyses | 61 | Major holdings & decisions |
| Key People | 7 | Investors & managers |
| Berkshire Letters | 60 | 1965-2024 complete |
| Partnership Letters | 35 | 1956-1970 complete |
| Special Letters | 3 | Historical documents |

---

## Trigger Keywords

The skill activates when your prompt contains any of these keywords:

### Chinese Triggers

巴菲特、芒格、格雷厄姆、B夫人、伯克希尔、Berkshire、护城河、安全边际、内在价值、市场先生、能力圈、复利、集中投资、管理层、竞争优势、低估、长期持有、价值投资、盖可保险、可口可乐、苹果、富国银行

### English Triggers

Buffett, Munger, Graham, Charlie, Ben, Berkshire, Berkshire Hathaway, moat, margin of safety, intrinsic value, Mr. Market, circle of competence, compounding, value investing, GEICO, Coca-Cola, Apple

---

## Data Sources

### Primary Sources

- **Berkshire Hathaway Shareholder Letters (1965-2024)**: Complete 60 annual letters
- **Partnership Letters (1956-1970)**: Complete 35 letters from Buffett's partnership era
- **Company Investment Records**: Historical decisions, entry/exit points, returns data

### Vault Maintenance

The Obsidian vault is maintained as part of the **花海 (Flowering Sea)** personal knowledge management system. Concept cards are cross-linked, regularly updated, and reviewed for consistency.

---

## Evaluation Results

Iteration 1 benchmark results (skill-enabled vs skill-free):

| Test Case | Assertions | Pass Rate | Skill vs No-Skill |
|---|---|---|---|
| Moat concept | 4/4 | 100% | 21% fewer tokens, 11s faster |
| Mr. Market allegory | 5/5 | 100% | 51% fewer tokens |
| Apple investment | 4/4 | 100% | More thorough, precise quotes |

---

## Contributing

### Extending the Vault

1. **Add new company analyses** — create `companies/[company-name].md` following existing format
2. **Improve concept cards** — enhance `concepts/[concept].md` with more quotes and examples
3. **Add missing letters** — add to `berkshire/` or `partnership/` if any are missing

### Concept Card Format

```markdown
# Concept Name

## 定位
> One-sentence definition

## 核心内容
(Content)

## 案例
(Optional)

## 操作要点
(Optional)

## links
in: [[related-card-a]], [[related-card-b]]
out: [[related-card-x]], [[related-card-y]]

## 来源
[[year-Letter Type]]
```

---

## License

MIT License

Copyright (c) 2026 changsheng-maker

This skill is not affiliated with Berkshire Hathaway, Warren Buffett, or any of his associated entities. It is an independent educational tool built on publicly available materials.

---

*中文版：[README.md](./README.md)*
