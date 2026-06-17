# Beginner Prompts

Use these prompts when explaining or running the workflow for beginners.

## 1. Create The Folder

```text
请帮我新建一个公文写作项目文件夹，里面按照以下结构整理：
samples/communications
samples/work-summaries
samples/reports
samples/notices
samples/speeches
samples/research-reports
edits/ai-drafts
edits/user-edited
profiles
source-materials/current-task
outputs
```

## 2. Train A Starter Style Profile

```text
请使用 personal-official-writing-workflow。
我已经把自己写过的材料放在：
{项目文件夹}/samples/{具体类型}

请先调用个人写作风格训练流程，帮我提炼这个场景的写作风格。
要求：
1. 只分析我自己的材料。
2. 输出 style-profile。
3. 输出我常用的结构、开头、段落习惯、常用表达和不喜欢的 AI 味表达。
4. 标注置信度：低/中/高。
```

## 3. Train From Before/After Edits

```text
请使用 personal-official-writing-workflow。
这里有 AI 初稿和我修改后的版本：
AI 初稿：{路径或文本}
我修改后的版本：{路径或文本}

请重点分析我改了什么，并把能复用的修改习惯更新到对应 style-profile。
```

## 4. Draft A New Material

```text
请使用 personal-official-writing-workflow 帮我写一份材料。

材料类型：{通讯稿/工作总结/汇报材料/通知/讲话稿/调研报告}
使用场景：{说明}
读者/接收对象：{说明}
必须保留的事实：{粘贴事实}
参考素材：{粘贴素材或文件路径}
使用的风格文件：{profiles/style-profile-xxx.md}
篇幅：{字数}
不能写的内容：{说明}

请先按我的个人风格写初稿，再按公文规范检查并修订。
```

## 5. Update After Human Revision

```text
这是 AI 生成稿：
{粘贴}

这是我最终修改稿：
{粘贴}

请把我的修改习惯沉淀为可复用规则，更新到对应 style-profile，并列出下次写作要避免的问题。
```

