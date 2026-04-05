# buffett-wisdom

**Warren Buffett investment wisdom assistant for Claude Code -- 基于巴菲特投资知识库的 AI 助手**

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
- [Data Sources \& Credits](#data-sources--credits)
- [Evaluation Results](#evaluation-results)
- [Contributing](#contributing)
- [License](#license)

---

## Installation

### Method 1: Drag and Drop (Easiest)

1. Download the `buffett-wisdom.skill` file from this repository
2. Open Claude Code
3. Drag the `.skill` file into the Claude Code window
4. The skill will be automatically installed and ready to use

### Method 2: Manual Installation

1. Clone or download this repository:
   ```bash
   git clone https://github.com/changsheng-maker/buffett-wisdom-skill.git
   ```
2. Copy `buffett-wisdom.skill` to your Claude Code skills directory:
   - macOS: `~/.claude/skills/`
   - Windows: `%USERPROFILE%\.claude\skills\`
   - Linux: `~/.claude/skills/`
3. Restart Claude Code

### Method 3: Git Symlink (For Development)

```bash
# Create a symlink to the skill in your Claude Code skills directory
ln -s /path/to/buffett-wisdom-skill/buffett-wisdom.skill ~/.claude/skills/buffett-wisdom.skill
```

---

## What It Does

**buffett-wisdom** is a Claude Code skill that transforms Claude into a Warren Buffett investment expert. It searches your personal Obsidian vault containing the complete collection of Buffett's writings to answer investment questions with precision and context.

### Core Features

| Feature | Description |
|---------|-------------|
| **Concept Explanations** | Deep explanations of Buffett concepts (护城河/安全边际/内在价值/市场先生/能力圈 etc.) with Buffett's exact words |
| **Quote Search** | Find Buffett's exact quotes on any topic across 98+ shareholder letters (1965-2024) |
| **Company Analysis** | Analyze companies using Buffett's investment framework (61 companies documented) |
| **Philosophy Application** | Apply Buffett's thinking to modern investment decisions |
| **Historical Context** | Track how Buffett's views evolved over different eras (1956-present) |
| **Cross-Reference** | Connect concepts, companies, and letters through rich linking |

### Supported Trigger Types

- **Concept questions**: "什么是护城河", "安全边际怎么用"
- **Philosophy questions**: "巴菲特怎么看市场波动", "为什么要长期持有"
- **Company questions**: "巴菲特为什么投苹果", "盖可保险好在哪"
- **Historical questions**: "1987股灾巴菲特做了什么", "他和芒格怎么认识的"
- **Application questions**: "用巴菲特的框架分析X公司", "这种情况巴菲特会怎么选"
- **Quote questions**: "巴菲特说过什么关于护城河的话", "他怎么描述市场先生"

---

## How It Works

The skill searches your Obsidian vault at `~/Documents/Obsidian/花海/04 Knowledge 知识网络/05 Topics 专题领域/09 巴菲特投资/` to find relevant information.

### Answering Strategy

1. **Identify the question type** -- concept, quote, company, philosophy application, or historical
2. **Targeted search** -- read the relevant concept card first, then find supporting letters/companies
3. **Synthesize** -- build the answer from:
   - The concept card's core definition
   - 2-3 powerful quotes from Buffett's own letters
   - Company cases or letter references
   - How Buffett's view evolved on this topic
   - Related concept links

### Response Style

- Start with the core insight in one sentence
- Use Buffett's own words where powerful
- Connect to concrete examples (GEICO, Coca-Cola, Washington Post are most-cited)
- End with the practical takeaway
- Reference the source concept card for further reading

---

## Usage Examples

### Example 1: Concept Explanation -- Moat (护城河)

**Prompt (Chinese):**
```
解释巴菲特的"护城河"概念，用他的话和实际案例说明
```

**What the skill does:**
- Reads `concepts/护城河.md` first
- Finds Buffett's 2007 letter quote about durable moats
- Identifies two types: low-cost (GEICO) and strong brand (Coca-Cola)
- Pulls specific investment return data points

**Expected output:**
> "护城河是巴菲特最核心的投资概念之一。2007年他在股东信中说：'一道需要不断重建的护城河，其实根本没有护城河。'他将护城河分为两种类型：低成本优势（如GEICO保险）和强品牌（如可口可乐）。GEICO的市场份额从2.5%增长到12%，正是护城河威力的证明。"
> — [[2007-巴菲特致股东信]]

---

### Example 2: Philosophy -- Mr. Market (市场先生)

**Prompt (Chinese):**
```
巴菲特怎么看市场波动？市场先生这个比喻是什么意思？
```

**What the skill does:**
- Reads `concepts/市场先生.md` for the allegory explanation
- Finds the 1987 letter quote about market being a servant not a guide
- Explains how volatility creates opportunity
- Gives the 1973 Washington Post example

**Expected output:**
> "市场先生来自格雷厄姆的《聪明的投资者》，不是巴菲特的发明，但巴菲特最爱用这个比喻。他说：'市场先生是来为你服务的，不是来引导你的。对你有用的是他的钱包，而不是他的智慧。'1973年华盛顿邮报大跌时，巴菲特看透了市场先生的情绪，反而大举买入。"
> — [[1987-巴菲特致股东信]]

---

### Example 3: Company Analysis -- Apple (苹果)

**Prompt (Chinese):**
```
巴菲特投资苹果的逻辑是什么？从他的股东信里找依据
```

**What the skill does:**
- Reads `companies/苹果.md` for investment thesis
- Cross-references with `concepts/护城河.md`
- Finds specific Apple quotes from Berkshire letters
- Analyzes brand loyalty and ecosystem as moat components

**Expected output:**
> "巴菲特投资苹果的核心逻辑是护城河。他看中的是苹果生态系统的忠诚度——用户一旦进入苹果生态，转换成本极高。2018年他在股东信中提到：'苹果产品的受欢迎程度令人难以置信，特别是对用户粘性的贡献。'这不是普通消费品的护城河，而是生态系统的护城河。"
> — [[2018-巴菲特致股东信]]

---

### Example 4: Quote Search

**Prompt (Chinese):**
```
巴菲特关于"安全边际"说过的最经典的话是什么？
```

**What the skill does:**
- Reads `concepts/安全边际.md`
- Finds the most powerful safety margin quotes
- Contextualizes when and why he said them

**Expected output:**
> "关于安全边际，最经典的可能是1987年他说的：'只有当潮水退去时，你才知道谁在裸泳。'这句话背后是安全边际的核心思想——永远要为不可预测的风险留足缓冲。"

---

### Example 5: Historical -- 1987 Crash

**Prompt (Chinese):**
```
1987年股灾时巴菲特做了什么？他怎么应对的？
```

**What the skill does:**
- Reads `berkshire/1987-巴菲特致股东信.md`
- Finds relevant sections on market crash response
- Explains his philosophical approach to volatility

**Expected output:**
> "1987年10月19日'黑色星期一'，道指暴跌22.6%。巴菲特的反应出奇平静——他几乎什么都没做。他在1987年信中解释：'我从不试图对市场走向做预测。如果你告诉我明天市场会大跌，我也不会有任何行动。'他的逻辑是：暴跌反而是机会，前提是你有现金和勇气。"

---

### Example 6: People -- Munger (芒格)

**Prompt (Chinese):**
```
巴菲特和芒格是什么关系？芒格如何影响巴菲特的投资哲学？
```

**What the skill does:**
- Reads `people/芒格.md`
- Traces the intellectual relationship
- Explains the shift from Graham-ism to quality-at-reasonable-price

**Expected output:**
> "芒格对巴菲特最大的影响是让他从'用便宜价格买普通公司'转向'用合理价格买优秀公司'。1972年，巴菲特本想卖掉喜诗糖果，芒格说服他留下。芒格说：'用合理的价格买一个伟大的公司，比用便宜的价格买一个普通的公司好得多。'这句话彻底改变了巴菲特的路径。"

---

### Example 7: Framework Application

**Prompt (Chinese):**
```
用巴菲特的框架分析比亚迪，为什么他买了又卖？
```

**What the skill does:**
- Reads `companies/比亚迪.md`
- Analyzes using Buffett's moat, circle of competence, and management frameworks
- Explains the buy and sell rationale

**Expected output:**
> "比亚迪是巴菲特唯一投资的中国公司，2008年买入，2022年开始减持。用他的框架看：新能源汽车的护城河在于电池成本和供应链管理，比亚迪早期符合能力圈，但随着中国新能源车竞争加剧，护城河受到侵蚀。巴菲特的卖出逻辑是：当竞争优势不再清晰时，纪律性减持。"

---

### Example 8: Concept Evolution

**Prompt (Chinese):**
```
巴菲特的"内在价值"概念是怎么演变的？
```

**What the skill does:**
- Reads `concepts/内在价值.md`
- Traces evolution across eras (Partnership 1956-1969, Transitional 1970-1989, Mature 1990-2009, Modern 2010-present)
- Shows how Buffett's definition deepened over time

**Expected output:**
> "'内在价值'在巴菲特眼中经历了三次演变。早期（1956-1969）他用Graham的清算价值法，简单粗暴。1970年代受芒格影响，他开始用'未来现金流折现'——这更接近今天的定义。进入伯克希尔成熟期（1990-2009），他说：'内在价值是一个公司在经营生涯中能产生的现金流的折现值。'这个定义至今未变。"

---

## Vault Structure

The skill draws from a carefully curated Obsidian vault at `~/Documents/Obsidian/花海/04 Knowledge 知识网络/05 Topics 专题领域/09 巴菲特投资/` containing:

```
09 巴菲特投资/
├── concepts/          # 49 concept cards
│   ├── 内在价值.md    # Intrinsic value
│   ├── 护城河.md      # Moat / competitive advantage
│   ├── 安全边际.md    # Margin of safety
│   ├── 市场先生.md     # Mr. Market
│   ├── 能力圈.md      # Circle of competence
│   ├── 保险浮存金.md  # Insurance float
│   ├── 集中投资.md    # Concentrated investment
│   ├── 管理层.md      # Management quality
│   ├── 复利.md        # Compounding
│   └── ...           # 40 more concepts
├── companies/         # 61 company analyses
│   ├── 苹果.md        # Apple
│   ├── 盖可保险.md    # GEICO
│   ├── 可口可乐.md    # Coca-Cola
│   ├── 富国银行.md    # Wells Fargo
│   ├── 华盛顿邮报.md  # Washington Post
│   └── ...           # 56 more companies
├── people/            # 7 key figures
│   ├── 芒格.md        # Charlie Munger
│   ├── 格雷厄姆.md    # Ben Graham
│   ├── B夫人.md       # Mrs. B (Nebraska Furniture Mart)
│   ├── 阿吉特·贾恩.md # Ajit Jain
│   └── ...           # 3 more figures
├── berkshire/         # 60 Berkshire shareholder letters (1965-2024)
│   ├── 1965-巴菲特致股东信.md
│   ├── 1987-巴菲特致股东信.md
│   ├── 2007-巴菲特致股东信.md
│   └── ...           # 1965-2024
├── partnership/       # 35 partnership letters (1956-1970)
│   ├── 1957-巴菲特致合伙人信.md
│   └── ...
├── special/           # 3 special letters
├── 巴菲特致股东信总览.md  # Master index
└── 巴菲特致股东信知识库.md # Knowledge base home
```

### Vault Statistics

| Category | Count | Coverage |
|----------|-------|----------|
| Concept Cards | 49 | Core investment concepts |
| Company Analyses | 61 | Major holdings & decisions |
| Key People | 7 | Investors & managers |
| Berkshire Letters | 60 | 1965-2024 complete |
| Partnership Letters | 35 | 1956-1970 complete |
| Special Letters | 3 | Historical documents |

---

## Trigger Keywords

The skill activates when your prompt contains any of these keywords (Chinese or English):

### Chinese Triggers

| Category | Keywords |
|----------|----------|
| Names | 巴菲特、芒格、格雷厄姆、B夫人 |
| Berkshire | 伯克希尔、Berkshire、巴菲特致股东信 |
| Core Concepts | 护城河、安全边际、内在价值、市场先生、能力圈 |
| Related Concepts | 复利、集中投资、管理层、竞争优势、低估、长期持有 |
| Philosophy | 价值投资、价值投资法、投资哲学 |
| Companies | 盖可保险、可口可乐、苹果、富国银行、华盛顿邮报、吉列 |
| Actions | 怎么投资、怎么分析、为什么买、为什么卖 |

### English Triggers

| Category | Keywords |
|----------|----------|
| Names | Buffett, Munger, Graham, Charlie, Ben |
| Berkshire | Berkshire, Berkshire Hathaway, Berkshire's letters |
| Core Concepts | moat, margin of safety, intrinsic value, Mr. Market, circle of competence |
| Related Concepts | compounding, concentrated investment, float, insurance float |
| Philosophy | value investing, investment philosophy, value investing approach |
| Actions | how would Buffett think, what would Buffett do, Buffett's view on |

---

## Data Sources & Credits

### Primary Sources

- **Berkshire Hathaway Shareholder Letters (1965-2024)**: Complete collection of 60 annual letters to shareholders
- **Partnership Letters (1956-1970)**: Complete collection of 35 letters from Buffett's partnership era
- **Company Investment Records**: Historical decisions, entry/exit points, returns data

### Data Provider

- Source website: https://buffett-letters-eir.pages.dev/
- Data scraped: 2026-04-05

### Vault Maintenance

The Obsidian vault is maintained as part of the **花海 (Flowering Sea)** personal knowledge management system. Concept cards are cross-linked, regularly updated, and reviewed for consistency.

### Citation Format

When using information from this skill, cite the specific letter or card:

```
巴菲特。[[2007-巴菲特致股东信]]

芒格。[[芒格]]

盖可保险投资案例。[[companies/盖可保险.md]]
```

---

## Evaluation Results

Benchmark results from Iteration 1 comparing skill-enabled vs skill-free responses:

### Test Case Results

| Test Case | Assertions | Pass Rate | Skill vs No-Skill |
|-----------|------------|-----------|-------------------|
| 护城河概念解释 | 4/4 | 100% | 节省21% tokens，快11秒 |
| 市场先生比喻 | 5/5 | 100% | 节省51% tokens |
| 苹果投资逻辑 | 4/4 | 100% | 更深入，引用精准 |

### Iteration 1 Conclusions

1. **Token Efficiency**: Skill version uses significantly fewer tokens (21-51% savings)
2. **Speed**: Faster response generation (up to 11 seconds improvement)
3. **Quality**: Answer depth maintained or improved with precise quotations
4. **Accuracy**: Cross-referenced answers reduce hallucinations

### Assertion Details

**护城河测试 (ID: 0):**
- [x] Contains 2007 letter quote about durable moats
- [x] Identifies two moat types (low-cost GEICO, brand Coca-Cola)
- [x] Includes specific investment return data
- [x] Links to related concepts

**市场先生测试 (ID: 1):**
- [x] Explains Mr. Market originates from Graham
- [x] Contains 1987 letter quote (servant not guide)
- [x] Explains volatility creates opportunity
- [x] Gives specific historical example
- [x] Links to related concepts

**苹果投资测试 (ID: 2):**
- [x] Uses moat framework for Apple analysis
- [x] Cites specific Buffett quotes from vault
- [x] Discusses brand loyalty and ecosystem as moat
- [x] Links to related concepts

---

## Contributing

### Extending the Vault

Contributions to improve the knowledge base are welcome:

1. **Add new company analyses** -- create `companies/[company-name].md` following the existing format
2. **Improve concept cards** -- enhance `concepts/[concept].md` with more quotes and examples
3. **Add missing letters** -- if any shareholder letters are missing, add them to `berkshire/` or `partnership/`
4. **Fix cross-links** -- ensure `## links` sections are properly bidirectional

### Concept Card Format

```markdown
# 概念名

## 定位
> 一句话定义

## 核心内容
（正文）

## 案例
（可选）

## 操作要点
（可选）

## links
in: [[相关卡片A]], [[相关卡片B]]
out: [[相关卡片X]], [[相关卡片Y]]

## 来源
[[年份-巴菲特致股东信]]
```

### Improving the Skill

To enhance the skill's behavior:

1. Edit `SKILL.md` to improve prompt handling
2. Update `evals/evals.json` to add new test cases
3. Test changes by running evaluation against new assertions

### Running Evaluations

```bash
# After modifying the skill, run evaluations
# (via Claude Code's built-in evaluation system)
```

---

## License

MIT License

Copyright (c) 2026 changsheng-maker

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

---

*This skill is not affiliated with Berkshire Hathaway, Warren Buffett, or any of his associated entities. It is an independent educational tool built on publicly available materials.*
