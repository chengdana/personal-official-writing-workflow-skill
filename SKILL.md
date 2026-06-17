---
name: personal-official-writing-workflow
description: Use when the user wants to train a personalized Chinese official-material writing style from their own drafts, revisions, communications, summaries, reports, notices, speeches, or government/enterprise materials, then draft or revise new materials with both personal voice and formal document standards.
---

# Personal Official Writing Workflow

## Overview

Build a reusable writing workflow for Chinese official materials by combining two separate capabilities:

- `learning-personal-writing-style`: learn how the user writes and revises from their own samples.
- `drafting-official-materials`: enforce document type, official structure, institutional tone, and quality checks.

This is not model fine-tuning. It is a local skill workflow based on samples, style profiles, revision rules, and official-material writing patterns.

This public package bundles the two required sub-skills under `skills/` so a reader can install the whole workflow from one repository.

## When To Use

Use this skill for:

- training a personal style profile from communications, summaries, reports, notices, speeches, research reports, briefings, or before/after edits
- drafting a new official material in the user's learned style
- revising an AI draft so it is both more like the user and more compliant with official-material conventions
- teaching a beginner how to set up a local writing project and use skills for office writing

Do not use this skill to imitate third-party authors without permission, fabricate policy basis, invent leaders' names, invent data, or replace human review for sensitive official documents.

## Required Sub-Skills

Load these only when the task reaches the matching stage. If the user's AI tool does not install sub-skills automatically, read the bundled files directly from this repository:

| Stage | Required skill | Bundled path | Purpose |
|-|-|-|-|
| Train or update style | `learning-personal-writing-style` | `skills/learning-personal-writing-style/SKILL.md` | Extract reusable style rules from user-owned samples and edits |
| Draft or revise official materials | `drafting-official-materials` | `skills/drafting-official-materials/SKILL.md` | Identify document type, structure the material, and check official tone/format |

## Recommended Project Folder

When the user has no existing folder, suggest this structure:

```text
official-writing-project/
├── samples/
│   ├── communications/
│   ├── work-summaries/
│   ├── reports/
│   ├── notices/
│   ├── speeches/
│   └── research-reports/
├── edits/
│   ├── ai-drafts/
│   └── user-edited/
├── profiles/
│   ├── style-profile-official.md
│   ├── style-profile-communication.md
│   ├── style-profile-summary-report.md
│   └── forbidden-patterns.md
├── source-materials/
│   └── current-task/
└── outputs/
```

Keep genres separate. Do not mix a newsletter-style communication, a work summary, a formal report, and a speech into one undifferentiated profile unless the user explicitly wants a rough starter profile.

## Workflow

1. **Set up samples**
   - Ask the user to place their own completed materials into the matching `samples/` folders.
   - Prefer 5-20 samples per genre. With 3-5 samples, mark confidence as starter-level.
   - Put AI draft vs user-edited pairs into `edits/`; these are the highest-value training material.

2. **Train style by scenario**
   - Use `learning-personal-writing-style`.
   - Build one profile per scenario when possible: communications, summaries/reports, speeches, research reports, notices.
   - Output `style-profile-*.md`, forbidden patterns, reusable outlines, and confidence.

3. **Draft from a real writing request**
   - Ask for the writing goal, document type if known, recipient/reader, source facts, must-keep wording, length, and deadline.
   - Use the closest style profile to draft the first version.
   - Preserve facts and mark missing information with `[待补充]`.

4. **Run the official-material pass**
   - Use `drafting-official-materials`.
   - Confirm whether the draft is a notice, report, request, letter, meeting minutes, speech, work summary, research report, or briefing.
   - Check structure, institutional relationship, policy/fact safety, official tone, headings, and closing formula.

5. **Learn from the user's edit**
   - When the user edits the output, compare AI draft vs user version with `learning-personal-writing-style`.
   - Add durable revision rules only when the edit reveals a repeatable preference.

## Input Contract

Before drafting, collect:

```text
材料类型：
使用场景：
读者/接收对象：
必须保留的事实：
参考素材：
希望接近的个人风格 profile：
篇幅：
不能写的内容：
```

If the user cannot provide all fields, continue with placeholders unless the missing field blocks the document type.

## Output Contract

For training:

```text
已读取样本：
生成/更新的风格文件：
风格置信度：
最明显的 5 条写作习惯：
需要继续补充的样本：
```

For writing:

```text
一、可直接修改的正文
二、已应用的个人风格规则
三、公文规范检查结果
四、待确认事项
五、建议回流训练的修改点
```

## Quality Rules

- Personal style can shape expression, rhythm, paragraphing, and preferred structures, but must not override document type, factual accuracy, or institutional tone.
- For strict statutory documents such as `请示`, `报告`, `通知`, `函`, and `会议纪要`, the official-material pass is mandatory after style drafting.
- For communications and briefings, readability may be stronger, but claims still need concrete facts, measures, effects, or next steps.
- Do not present a starter profile as stable. State confidence based on sample count and edit quality.
- Keep beginner-facing guidance step-by-step. Avoid assuming the user understands skills, local folders, Markdown, or style profiles.

## Common Mistakes

| Mistake | Fix |
|-|-|
| Putting all sample materials into one folder | Separate by scenario before training |
| Training only from final drafts | Add AI draft vs user-edited pairs whenever possible |
| Drafting in personal style but skipping official checks | Always run `drafting-official-materials` before delivery |
| Letting the model invent policy/data | Use placeholders and ask for confirmation |
| Updating style after every tiny edit | Update only repeatable preferences; keep one-off edits as notes |
