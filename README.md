# Personal Official Writing Workflow Skill

一个面向中文办公、公文、通讯稿、总结报告、汇报材料写作的公开 Skill。

它把两类能力串成一个轻量工作流：

- 先用你自己的历史材料训练个人写作风格。
- 再用公文/正式材料规范检查结构、语气、事实边界和格式。

## 适合谁

- 经常写通讯稿、总结、汇报、通知、讲话稿、调研报告的人。
- 希望 AI 学会自己的表达习惯，而不是每次都写出很重 AI 味的人。
- 希望把个人写作风格和正式材料规范结合起来的人。

## 安装方式

在 Trae、Claude Code、Codex 等支持 Skills 的 AI 工具中，输入：

```text
请安装该链接中的 Skill，确保适配我的平台的 Skill 安装规范：
https://github.com/chengdana/personal-official-writing-workflow-skill
```

安装完成后，重启你的 AI 工具。

之后可以通过 `/personal-official-writing-workflow` 调用这个 Skill。

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

## 文件结构

```text
personal-official-writing-workflow-skill/
├── SKILL.md
├── references/
│   └── beginner-prompts.md
├── README.md
└── LICENSE
```

## 隐私提醒

这个仓库只包含 Skill 工作流和提示词模板，不包含任何 API Key、账号密码、cookie、token 或个人材料样本。

训练个人写作风格时，请只使用你自己有权使用的材料。涉及单位内部材料、敏感数据或未公开信息时，不要上传到公开仓库。

