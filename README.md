# cn-en-format

Markdown 中英混排格式化 skill，用于 Claude Code。

## 功能

自动检测和修复 Markdown 文件中的中英混排排版问题：

- **空格**：中英之间、中文与数字之间、引号外、行内代码前后
- **标点**：中文语境全角标点、弯引号、顿号
- **标题**：GFM 兼容的 `#` 后空格
- **数字**：单位无空格、范围用 `~`

## 用法

在 Claude Code 中调用此 skill 后，对话中输入 Markdown 文件路径即可：

```
/cn-en-format 我的文章.md
```

或描述需求：

```
帮我修复这篇文章的中英混排格式
```

## 设计原则

- **只改格式，不改内容** — 不增删实质信息
- **边界优先** — 代码块、URL、frontmatter、双链等区域不动
- **规则可追溯** — 每条修改都有明确规则依据

## 参考

- [markdown-writing-with-mixed-cn-en](https://github.com/selfteaching/markdown-writing-with-mixed-cn-en) — 规则来源，取其精华去其糟粕
- GB/T 15834《标点符号用法》— 全角标点规范参考

## 许可

MIT
