# Personal Official Writing Workflow Skill Pack

一个面向中文办公、公文、通讯稿、总结报告、汇报材料写作的公开 Skill 包。

它不是只有一个“总控 Skill”，而是把三部分打包在一起：

| 部分 | 作用 |
|-|-|
| `personal-official-writing-workflow` | 总控工作流：负责串联训练、起草、规范检查和回流学习 |
| `learning-personal-writing-style` | 个人风格训练：从你自己的历史材料和改稿中提炼写作习惯 |
| `drafting-official-materials` | 公文规范写作：检查正式材料的文种、结构、语气、事实边界和格式 |

## 适合谁

- 经常写通讯稿、总结、汇报、通知、讲话稿、调研报告的人。
- 希望 AI 学会自己的表达习惯，而不是每次都写出很重 AI 味的人。
- 希望把个人写作风格和正式材料规范结合起来的人。

## 安装方式

在 Trae、Claude Code、Codex 等支持 Skills 的 AI 工具中，输入：

```text
请安装该链接中的 Skill 包，确保同时安装里面的主 Skill 和两个子 Skill，并适配我的平台的 Skill 安装规范：
https://github.com/chengdana/personal-official-writing-workflow-skill
```

安装完成后，重启你的 AI 工具。

之后可以通过 `/personal-official-writing-workflow` 调用总控 Skill。

如果你的平台不支持 `/` 调用，也可以直接输入：

```text
请使用 personal-official-writing-workflow。
```

## 推荐使用流程

1. 新建一个写作项目文件夹。
2. 把自己写过的材料按场景分类放进去。
3. 调用这个 Skill，先训练个人写作风格。
4. 给出新的写作任务和素材，让 AI 按你的风格写初稿。
5. 再让 Skill 按公文/正式材料规范检查和修订。
6. 把你最终人工修改后的版本回流给 Skill，让它继续学习你的写法。

## 材料怎么放

建议先在电脑里建一个总文件夹，例如：`D盘 / 程大拿写作`。

然后按常见材料类型建子文件夹，例如：

```text
活动通讯稿
年度工作总结
向上级汇报材料
工作通知
领导讲话稿
调研报告
```

每个类型文件夹里，再建三个小文件夹：

```text
我写过的定稿
AI初稿
我修改后的版本
```

如果有 AI 初稿和你修改后的版本，建议用同一个编号保存成一组：

```text
001-支行客户活动通讯稿-AI初稿.docx
001-支行客户活动通讯稿-我修改后.docx
```

同一个编号，代表同一次写作任务。这样 Skill 后续可以对比“AI 原来怎么写”和“你实际怎么改”，更容易学到你的真实写作习惯。

## 写新材料时怎么提需求

如果你不知道该选哪种材料类型、也不记得自己有哪些风格说明，不用自己硬填。

你先只说一句：

```text
请使用 personal-official-writing-workflow 帮我写一份材料。
```

接下来，Skill 会引导你补充这些信息：

1. 材料类型：工作总结 / 汇报材料 / 通讯稿 / 通知 / 讲话稿
2. 使用场景：季度工作推进情况总结 / 活动结束后通讯稿 / 个人表态讲话稿
3. 大致框架：你想写哪几部分，以及必须保留的事实
4. 参考素材：参考材料路径，或直接粘贴内容
5. 文字篇幅：大概多少字
6. 不能写的内容：例如不能编造数据、不能写没有依据的表态

Skill 写出初稿后，先保存一份 AI 生成稿，再另存一份给自己修改。不要直接覆盖 AI 生成稿。

例如：

```text
年度工作总结 / AI初稿 / 002-季度工作总结-AI生成稿.docx
年度工作总结 / 我修改后的版本 / 002-季度工作总结-我修改后.docx
```

后续让 Skill 对比这两份文件，它才能学到你的修改习惯。

## 文件结构

```text
personal-official-writing-workflow-skill/
├── SKILL.md
├── references/
│   └── beginner-prompts.md
├── skills/
│   ├── learning-personal-writing-style/
│   │   ├── SKILL.md
│   │   ├── references/
│   │   └── scripts/
│   └── drafting-official-materials/
│       ├── SKILL.md
│       └── references/
├── README.md
└── LICENSE
```

如果你的 AI 工具只安装根目录的 `SKILL.md`，总控 Skill 也会提示它读取 `skills/` 里的两个子 Skill 文件；如果你的平台支持批量安装 Skill 包，则建议同时安装三个 Skill。

## 隐私提醒

这个仓库只包含 Skill 工作流、参考文档和轻量脚本，不包含任何 API Key、账号密码、cookie、token 或个人材料样本。

训练个人写作风格时，请只使用你自己有权使用的材料。涉及单位内部材料、敏感数据或未公开信息时，不要上传到公开仓库。
