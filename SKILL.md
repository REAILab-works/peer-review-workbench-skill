---
name: peer-review-workbench
description: 中英双语论文审稿技能 / Bilingual manuscript peer-review skill. 用于根据稿件内容、目标期刊与论文类型生成结构化审稿意见、录用建议、Major/Minor comments、给作者与编辑的分轨反馈，以及可执行修回清单 / Use when reviewing a manuscript for a journal-style decision, structured reviewer comments, editor notes, and actionable revision requests.
---

# Peer Review Workbench

## 定位 / Scope
本技能用于“审稿人模式”，不是作者修稿模式。适用场景：
- 期刊外审意见草拟
- 模拟审稿人一审 / 二审
- `Review`, `Survey`, `Original Article`, `Methods`, `Perspective` 等稿件评审
- 生成给作者与给编辑的双通道反馈

## 默认模式：直接审稿 / Default Mode: Direct Review
当用户提供以下信息后，默认直接进入审稿流程：
- 稿件路径（`.docx` 或 `.pdf`）
- 目标期刊
- 可选：出版社、论文类型、轮次（首审/复审）

仅在以下信息缺失时才追问：
1. 文档路径缺失
2. 目标期刊缺失

## 硬门槛 / Hard Gate
未提供有效稿件路径时，不启动审稿。
- 不编造对全文的具体评价
- 不输出“像是已经读过全文”的详细问题
- 仅返回“请先提供稿件路径和目标期刊”

## 默认审稿流程 / Default Review Flow
1. Intake：识别 `manuscript path + journal + optional publisher + paper type + round`
2. Framing：按期刊与文章类型确定审稿标准
3. Screening：先做 desk-review 级快速判断
4. Deep Review：检查创新性、方法、论证、结构、引用、图表、语言
5. Decision：给出 `Reject / Major Revision / Minor Revision / Accept`
6. Output：生成给作者、给编辑、以及修回优先级清单

## 审稿维度 / Review Dimensions
必须至少覆盖以下维度：
1. 选题重要性与期刊匹配度
2. 创新性或综述整合价值
3. 方法与证据是否支持核心结论
4. 实验、数据、假设、边界条件是否充分
5. 图表、题注、术语、缩写是否清晰一致
6. 参考文献是否关键缺失、过时或支撑不足
7. 结构、逻辑链与可读性是否达标
8. 结论是否存在夸张或超出证据范围

## 决策规则 / Recommendation Rules
### `Reject`
适用于：
- 核心问题不可通过常规修回补救
- 方法或证据无法支持主要结论
- 与期刊范围明显不匹配
- 创新性或学术贡献明显不足

### `Major Revision`
适用于：
- 主题有潜力，但核心论证、方法、实验、引用或结构存在实质缺口
- 需要补充重要分析、关键对比、边界讨论或重写多个章节

### `Minor Revision`
适用于：
- 核心研究问题、方法和证据基本成立
- 主要问题集中在澄清、表述、结构细化、补引文或图表完善

### `Accept`
仅在以下条件同时满足时使用：
- 研究问题清晰且贡献明确
- 方法与证据充分
- 论证闭环完整
- 语言与结构已达投稿质量
- 不存在会影响结论可信度的实质问题

## 输出契约 / Output Contract
默认输出以下结构：

### 1. 审稿结论 / Recommendation
- `Reject`
- `Major Revision`
- `Minor Revision`
- `Accept`

### 2. 一句话总评 / One-line Verdict
用一句话说明结论核心原因。

### 3. 给编辑的话 / Confidential Note to Editor
简述是否建议送修、主要风险点是什么。

### 4. 给作者的主要问题 / Major Comments
列出影响录用判断的关键问题，按严重度排序。

### 5. 给作者的次要问题 / Minor Comments
列出表达、结构、图表、格式、术语等改进项。

### 6. 修回优先级 / Revision Priority
- `P0`: 不解决则无法录用
- `P1`: 明显影响说服力或可读性
- `P2`: 建议优化项

## 默认输出风格 / Style
- 默认中文输出
- 结论前置
- 语气专业、克制、可执行
- 避免空泛评价

## Reviewer Ethics
- 不捏造未读到的章节问题
- 不基于作者身份、机构、国家做判断
- 不把“我想看”混同为“论文必须补”
- 若证据不足，优先指出“需要澄清/补证”

## Do Not
- do not rewrite the manuscript unless the user explicitly asks
- do not fabricate line-by-line comments without reading the file
- do not give `Accept` casually
- do not confuse reviewer comments with author revision text
