# Beginner Prompts

Use these prompts when explaining or running the workflow for beginners.

## 1. Create The Folder

```text
请帮我新建一个公文写作项目文件夹。

例如：
D盘 / 程大拿写作

请先按材料类型创建子文件夹：
活动通讯稿
年度工作总结
向上级汇报材料
工作通知
领导讲话稿
调研报告

每个材料类型文件夹下面，再创建四个子文件夹：
我写过的定稿
AI原始初稿
AI规范修订稿
我最终修改稿
```

## 2. Train A Starter Style Profile

```text
请使用 personal-official-writing-workflow。
我已经把自己写过的材料放在：
{项目文件夹}/{材料类型}/我写过的定稿

请先调用个人写作风格训练流程，帮我提炼这个场景的写作风格。
要求：
1. 只分析我自己的材料。
2. 输出 style-profile。
3. 输出我常用的结构、开头、段落习惯、常用表达和不喜欢的 AI 味表达。
4. 标注置信度：低/中/高。
```

## 3. Train From Three Draft Versions

```text
请使用 personal-official-writing-workflow。
这里有同一次写作任务的三份稿件：
AI原始初稿：{路径或文本}
AI规范修订稿：{路径或文本}
我最终修改稿：{路径或文本}

请先说明：AI原始初稿到AI规范修订稿，主要修了哪些公文规范问题。
再重点分析：AI规范修订稿到我最终修改稿，我改了什么。
只把第二类里面能复用的个人修改习惯更新到对应 style-profile。
```

## 4. Draft A New Material

```text
请使用 personal-official-writing-workflow 帮我写一份材料。

材料类型：{通讯稿/工作总结/汇报材料/通知/讲话稿/调研报告}
使用场景：{说明}
读者/接收对象：{说明}
必须保留的事实：{粘贴事实}
参考素材：{粘贴素材或文件路径}
篇幅：{字数}
不能写的内容：{说明}

请自动匹配最接近的材料类型风格说明。
请先按我的个人风格写AI原始初稿，再按公文规范检查并形成AI规范修订稿。
如果你可以操作本地文件，请分别保存到对应文件夹。
```

## 5. Update After Human Revision

```text
请使用 personal-official-writing-workflow，帮我更新写作风格。

AI原始初稿：
{路径或文本}

AI规范修订稿：
{路径或文本}

这是我最终修改稿：
{路径或文本}

请先区分公文规范修订和个人修改偏好。
个人风格只重点参考AI规范修订稿到我最终修改稿之间的变化。
请把能复用的修改习惯沉淀为规则，更新到对应 style-profile，并列出下次写作要避免的问题。
```
