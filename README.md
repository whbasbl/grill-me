# Grill Me

这两个 Codex skill 用来通过持续追问，帮助你澄清和打磨计划、设计或想法。

## 两个 skill 的关系

- **`grill-me`** 是入口 skill。明确调用它时，会转交给 `grilling`，因此使用入口时两个 skill 都必须安装。
- **`grilling`** 是实际执行访谈的 skill：它将待决定事项组织成决策树，逐轮提出当前可以回答的问题，并根据你的回答继续展开。
- 也可以直接调用 `grilling`，不经过入口。

## 作者与来源

原作者是 [Matt Pocock](https://github.com/mattpocock)。这两个 skill 来自他的 [`mattpocock/skills`](https://github.com/mattpocock/skills) 项目。随附的 `LICENSE` 保留了上游 MIT 许可及版权声明。

## 在 Codex 中全局安装

Codex 官方文档将个人 skill 目录定义为 `$HOME/.agents/skills`。把每个 skill 目录（其中包含 `SKILL.md`）放到该目录下，即可在不同项目中使用。以下命令会安装这两个 skill：

```sh
git clone https://github.com/whbasbl/grill-me.git
mkdir -p ~/.agents/skills
cp -R grill-me/skills/grill-me grill-me/skills/grilling ~/.agents/skills/
```

Codex 会自动检测新 skill；如果没有显示，请重启 Codex。可在 Codex CLI 或 IDE 扩展中输入 `/skills` 查看可用 skill。

## 使用

在 Codex CLI 或 IDE 扩展的提示中输入 `$grill-me`，使用入口 skill；或输入 `$grilling`，直接启动访谈。随后描述你希望打磨的计划、设计或想法，并逐轮回答问题。

参考：[Codex 官方 Skills 文档](https://developers.openai.com/codex/skills/)（个人安装位置、检测方式及 `$skill-name` 显式调用说明）。
