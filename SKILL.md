---
name: buffett-wisdom
description: Warren Buffett investment wisdom assistant. Use when user asks about Buffett, Berkshire Hathaway, investment philosophy, specific investment concepts (护城河/安全边际/内在价值/市场先生 etc.), wants Buffett's view on a company or decision, or asks to apply Buffett's thinking to any question. Trigger on "巴菲特", "Buffett", "Berkshire", "价值投资", "安全边际", "护城河" and any question about Buffett's investment approach.
---

# Buffett Wisdom Skill

Answers questions about Warren Buffett's investment philosophy using the Obsidian vault at `~/Documents/Obsidian/花海/04 Knowledge 知识网络/05 Topics 专题领域/09 巴菲特投资/`.

## Vault Structure (for searching)

```
09 巴菲特投资/
├── concepts/          # 49 concept cards (内在价值, 护城河, 安全边际, 市场先生, 复利...)
├── companies/         # 61 company analyses (盖可保险, 可口可乐, 苹果, 富国银行...)
├── people/            # 7 key figures (芒格, 格雷厄姆, B夫人, 阿吉特·贾恩...)
├── berkshire/         # 60 Berkshire shareholder letters (1965-2024), named 2017-巴菲特致股东信.md
├── partnership/       # 35 partnership letters (1956-1970)
├── special/           # 3 special letters
├── 巴菲特致股东信总览.md  # Master index
└── 巴菲特致股东信知识库.md # Knowledge base home
```

## How to Answer Questions

### Step 1: Identify what the user needs
- **Concept explanation**: User wants to understand 内在价值, 护城河, 安全边际, 市场先生, 能力圈, etc.
- **Quote search**: User wants Buffett's exact words on a topic
- **Company question**: User asks about a specific company through Buffett's lens
- **Philosophy application**: User asks "should I invest in X" or "what would Buffett think about Y"
- **Evolution question**: User asks how Buffett's thinking changed over time

### Step 2: Search the vault
Read the relevant concept card first, then find supporting letters/companies as needed.

**Core concepts to check first** (always read these when relevant):
- `concepts/内在价值.md` — intrinsic value, the foundation of everything
- `concepts/护城河.md` — moat, competitive advantage
- `concepts/安全边际.md` — margin of safety
- `concepts/市场先生.md` — Mr. Market
- `concepts/能力圈.md` — circle of competence
- `concepts/保险浮存金.md` — insurance float
- `concepts/集中投资.md` — concentrated investment
- `concepts/管理层.md` — management quality
- `concepts/复利.md` — compounding

**Search pattern for concepts**: `pattern` on `concepts/*.md` in the vault directory
**Search pattern for companies**: `pattern` on `companies/*.md` in the vault directory
**Search pattern for letters**: `pattern` on `berkshire/*.md` or `partnership/*.md`

### Step 3: Synthesize

Build your answer from:
1. **The concept card's core definition** — what it means in Buffett's own framing
2. **Key quotes** — pull 2-3 of the most illustrative quotes from the concept card
3. **Supporting examples** — company cases or letter references from the concept card
4. **Evolution** — how Buffett's view on this concept evolved (check the concept card's 历史 section)
5. **Links** — reference related concepts from the card's `## links` section

### Response Style
- Start with the core insight in one sentence
- Use Buffett's own words where powerful
- Connect to concrete examples (盖可保险, 可口可乐, 华盛顿邮报 are the most-cited)
- End with the practical takeaway
- Always link to the source concept card for further reading

## Concept Evolution Format

When asked about how Buffett's thinking evolved, organize by era:
- **Early Partnership (1956-1969)**: Pure Graham-style, focus on tangible asset discounts
- **Transitional (1970-1989)**: Munger influence, shift to quality at reasonable price
- **Mature Berkshire (1990-2009)**: Systematic compounding, insurance float maximization
- **Modern (2010-present)**: Share buybacks, mega-cap era, succession

## Quote Formatting

Format quotes like this:
> "[exact quote from the text]"
> — [letter reference in brackets]

Example:
> "市场先生是来为你服务的，不是来引导你的。对你有用的是他的钱包，而不是他的智慧。"
> — [[1987-巴菲特致股东信]]

## Company Analysis Pattern

When analyzing a company using Buffett's framework:
1. Does it have a durable moat (护城河)? What type — low-cost or strong brand?
2. Is it within Buffett's circle of competence (能力圈)?
3. Can you estimate intrinsic value (内在价值) roughly? Is there a margin of safety (安全边际)?
4. Is management honest and capable (管理层)?
5. Does it compound capital (复利) over time?

## Common User Questions & Vault Strategy

| Question Type | Where to Search | What to Read |
|---|---|---|
| "什么是护城河" | concepts/护城河.md | Full card, pull 3 key quotes |
| "巴菲特怎么看市场波动" | concepts/市场先生.md + berkshire/1987*.md | Mr. Market card + 1987 letter |
| "为什么要长期持有" | concepts/长期持有.md + concepts/复利.md | Both cards |
| "巴菲特怎么分析苹果" | companies/苹果.md + concepts/护城河.md | Apple card + moat concept |
| "1987股灾巴菲特做了什么" | berkshire/1987-巴菲特致股东信.md | Full letter, relevant sections |
| "巴菲特和芒格的关系" | people/芒格.md | Full card |
| "盖可保险为什么重要" | companies/盖可保险.md + concepts/保险浮存金.md | Both cards |

## Important Notes
- Concept cards contain extensive cross-links — always read the `## links` section
- Company cards contain the full history with specific investment years and returns
- Letter files are long — use grep to find the relevant section first
- The vault has ~220 files — use targeted searches, not full directory reads
