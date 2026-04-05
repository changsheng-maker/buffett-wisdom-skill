# buffett-wisdom

Warren Buffett investment wisdom skill for Claude Code.

## 安装

将 `buffett-wisdom.skill` 文件拖入 Claude Code 安装。

## 功能

回答巴菲特投资相关问题，基于完整收录的98封巴菲特致股东信（1956-2024）：

- **核心概念解释**：护城河、安全边际、内在价值、市场先生、能力圈、保险浮存金、复利、集中投资等
- **巴菲特原话引用**：来自1957-2024年所有致股东信
- **公司分析框架**：盖可保险、可口可乐、苹果、富国银行等61家公司
- **关键人物**：芒格、格雷厄姆、B夫人、阿吉特·贾恩等

## 触发词

巴菲特、Buffett、Berkshire、价值投资、安全边际、护城河 等

## 数据来源

- 花海 Obsidian Vault 中的巴菲特投资专题
- 来源：https://buffett-letters-eir.pages.dev/
- 抓取日期：2026-04-05

## 评估结果

| 测试用例 | 通过率 | Skill vs 无Skill |
|---|---|---|
| 护城河概念解释 | 4/4 ✅ | 省21% tokens，快11秒 |
| 市场先生比喻 | 5/5 ✅ | 省51% tokens |
| 苹果投资逻辑 | 4/4 ✅ | 更深入，引用精准 |

**迭代1结论**：Skill版本在tokens效率上更优，答案质量与无skill版持平。
