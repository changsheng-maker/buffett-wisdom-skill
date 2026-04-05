# Buffett Reasoning Chains

Structured thinking patterns for answering investment questions through Buffett's framework.

---

## Chain 1: "Is This a Good Investment?"

Use this when user asks "Should I invest in X?" or "分析一下这只股票"

```
Step 1 → 护城河 (Moat)
  Read: concepts/护城河.md
  Ask: Does X have a durable competitive advantage? What type?
    - Low-cost producer? (Check: companies/盖可保险.md)
    - Strong brand? (Check: companies/可口可乐.md, companies/苹果.md)
    - Network effect? (Check: concepts/护城河.md for examples)
  Key test: "Would a competitor need to rebuild this moat every year?"

Step 2 → 内在价值 (Intrinsic Value)
  Read: concepts/内在价值.md
  Ask: Can you estimate X's intrinsic value? Is price vs value gap clear?
  Buffett formula: "Cash flows over lifetime discounted at appropriate rate"
  Key test: "Is this business a 'cash-producing machine'?"

Step 3 → 安全边际 (Margin of Safety)
  Read: concepts/安全边际.md
  Ask: Is price significantly below intrinsic value?
  Key test: "If I'm wrong about my estimate, is there enough cushion?"

Step 4 → 能力圈 (Circle of Competence)
  Read: concepts/能力圈.md
  Ask: Do I understand X's business well enough to estimate its future cash flows?
  Key test: "Could I explain X's business model to a smart 10-year-old?"

Step 5 → 管理层 (Management)
  Read: concepts/管理层.md
  Ask: Is management honest, capable, and shareholder-oriented?
  Key test: "Would I trust this CEO with my family money?"

Step 6 → 复利 (Compounding)
  Read: concepts/复利.md
  Ask: Will this business compound capital reliably over time?
  Key test: "Will I want to hold this for 10+ years?"
```

**Output format:**
```
# 投资分析：[公司/股票名称]

## 护城河判定
[Type] — [Evidence from vault]
Verdict: [Strong/Weak/Uncertain]

## 内在价值估算
[DCF approximation or analogical reasoning]
Price vs Value: [Significant gap / Reasonable / Expensive]

## 安全边际
[Calculation or reasoning]
Margin: [Wide enough / Too narrow]

## 能力圈
[Explanation of understanding level]
Verdict: [In circle / Borderline / Outside circle]

## 管理层评估
[Evidence from vault or general principle]
Verdict: [Excellent/Good/Poor]

## 复利潜力
[Analysis]
Verdict: [High compounding / Moderate / Poor]

## 综合结论
[One paragraph synthesis]
Buffett-style verdict: [Buy/Don't Buy/Watch]
```

---

## Chain 2: "What Would Buffett Think About X?"

Use when user asks "巴菲特怎么看X" or "What would Buffett say about X?"

```
Step 1: Find Buffett's public statements about similar industries
  → Search berkshire/*.md for similar company types
  → Check concepts/行业name.md if industry card exists

Step 2: Map X to Buffett's known framework
  → Consumer franchise? → See Coca-Cola, See's Candy
  → Low-cost operator? → See GEICO, Costco
  → Financial institution? → See Wells Fargo, Bank of America
  → Tech with durable moat? → See Apple (the exception)

Step 3: Identify applicable core principles
  → Check relevant concept cards in vault
  → Look for direct quotes on topic type

Step 4: Find cautionary tales
  → Search for Dexter Shoes (moat destroyed by overseas competition)
  → Search for airline investments (destroyed capital despite growth)
  → Search for LTCM lessons (leverage + genius = danger)

Step 5: Synthesize through Buffett's mental model
  Key filters: "Is this durably simple?" + "Can I estimate future cash flows?" + "Is price right?"
```

**Output format:**
```
# Buffett会怎么看：[X]

## 已知类比
Buffett has said/done similar things involving: [Company/Industry from vault]

## 适用原则
From the vault, Buffett's documented position on this type of investment:

> "[Relevant quote from vault]"
> — [Source letter]

## 会加分的地方
[Positive factors through Buffett's lens]

## 会扣分的地方
[Red flags through Buffett's lens]

## 最可能的结论
[Synthesized Buffett-style verdict with reasoning]

## 原话引用
[Any exact Buffett quotes found in vault on this topic]
```

---

## Chain 3: "How Did Buffett's Thinking Evolve on X?"

Use when user asks "巴菲特的理念是怎么演变的" or "Buffett早期和现在的想法有什么不同"

```
Period 1 — 合伙人时期 (1956-1969)
  Read: partnership/*.md (especially 1961, 1962, 1964, 1965)
  Character: Pure Graham-style, cigar-butt investing, tangible asset discounts
  Key theme: "Buy cheap businesses, diversify"

Period 2 — 转变期 (1970-1989)
  Read: berkshire/1977-1989.md, concepts/芒格.md
  Character: Munger's influence, quality over quantity
  Key theme: "Buy wonderful businesses at fair prices"
  Inflection point: 喜诗糖果 acquisition (1972)

Period 3 — 成熟伯克希尔 (1990-2009)
  Read: berkshire/1990-2009.md, concepts/透视盈余.md
  Character: Insurance float maximization, mega-cap compounding
  Key theme: "Durable moats + patient capital"

Period 4 — 现代 (2010-2025)
  Read: berkshire/2016-2024.md
  Character: Share buybacks as capital allocation tool, mega-cap tech (Apple)
  Key theme: "Clone ourselves at low cost through buybacks"
```

**Output format:**
```
# 巴菲特在[Topic]上的思想演变

## 早期观点 (1956-1969)
[From partnership letters — pure Graham approach to this topic]

## 转变 (1970-1989)
[From Munger influence — shift toward quality]

## 成熟期 (1990-2009)
[Systematic, principled approach — what he came to believe definitively]

## 近期 (2010-2025)
[How current view differs from past — nuances, exceptions, refinements]

## 一句话总结
[The final Buffett consensus on this topic]
```

---

## Chain 4: "Extract Buffett's Exact Quote on X"

Use when user wants specific Buffett quotes

```
Step 1: Search concept cards
  → Grep concepts/*.md for topic keyword
  → Concept cards contain curated quotes with context

Step 2: Search letters for year-specific quotes
  → grep berkshire/*.md for topic
  → Partnership letters: grep partnership/*.md

Step 3: Verify attribution
  → Confirm: Year + Letter type (致股东信/致合伙人信)
  → Confirm: Context (what was happening when he said this)

Step 4: Format for readability
```

**Quote formatting template:**
```
> "[Exact Chinese translation of quote]"
> — [Year] [Letter type], [Context/occasion]

来源：[File in vault]

[1-2 sentence explanation of why this quote matters]
```

---

## Chain 5: "Compare Two Investments"

Use when user asks "A和B哪个更像巴菲特会投的"

```
Step 1: Apply Investment Decision Chain to A
  → Full 6-step analysis above
  → Score: Moat [Strong/Weak], IV [Clear/Unclear], Safety [Wide/Tight], Circle [In/Out], Mgmt [Excellent/Good/Poor], Compound [High/Med/Low]

Step 2: Apply Investment Decision Chain to B
  → Same 6 steps

Step 3: Direct comparison
  | Dimension | A | B |
  |---|---|---|
  | 护城河 | | |
  | 内在价值 | | |
  | 安全边际 | | |
  | 能力圈 | | |
  | 管理层 | | |
  | 复利潜力 | | |

Step 4: Verdict
  "Buffett would more likely choose [A/B] because..."
  "The deciding factor is..."
```

---

## Quick Reference: Vault File Map

| Question Type | Primary File | Supporting Files |
|---|---|---|
| 护城河定义 | concepts/护城河.md | companies/盖可保险.md, companies/可口可乐.md |
| 内在价值 | concepts/内在价值.md | berkshire/1989-*.md, berkshire/1992-*.md |
| 安全边际 | concepts/安全边际.md | concepts/低估.md, berkshire/1992-*.md |
| 市场先生 | concepts/市场先生.md | berkshire/1987-*.md, berkshire/1993-*.md |
| 能力圈 | concepts/能力圈.md | berkshire/1996-*.md, concepts/管理层.md |
| 保险浮存金 | concepts/保险浮存金.md | companies/盖可保险.md, berkshire/2010-*.md |
| 芒格 | people/芒格.md | concepts/喜诗糖果.md, concepts/内在价值.md |
| 格雷厄姆 | people/格雷厄姆.md | concepts/安全边际.md, concepts/市场先生.md |
| 苹果 | companies/苹果.md | berkshire/2018-*.md through 2024-*.md |
| 可口可乐 | companies/可口可乐.md | berkshire/1988-*.md, berkshire/1993-*.md |
| 盖可保险 | companies/盖可保险.md | concepts/保险浮存金.md, concepts/护城河.md |
