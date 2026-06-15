# Shownotes Skill

这是一个 Codex skill，用于把播客文字稿、字幕文件或带说话人标签的文本，整理成可发布的 shownotes 和不同平台需要的节目文案。

## 可以生成什么

- 网站版节目 shownotes
- Apple Podcasts 节目简介
- 带章节时间戳的 YouTube 简介
- Newsletter 预告文案
- 社交媒体片段
- 给编辑复核用的风险提示和假设说明

## 安装

把这个仓库复制到 Codex skills 目录：

```sh
mkdir -p ~/.codex/skills/shownotes
cp -R SKILL.md agents references ~/.codex/skills/shownotes/
```

然后在 Codex 中这样使用：

```text
Use $shownotes to turn this podcast transcript into website show notes and platform-specific episode descriptions.
```

也可以直接用中文描述需求，例如：

```text
使用 $shownotes，把这份播客文字稿整理成网站 shownotes、Apple Podcasts 简介和 YouTube 时间戳简介。
```

## 文件结构

- `SKILL.md` 定义这个 skill 的触发场景和工作流程。
- `references/output-schema.md` 提供字段级输出模板和人工复核清单。
- `agents/openai.yaml` 保存展示名称、简短说明和默认提示词。

## 使用原则

这个 skill 的目标不是替代编辑判断，而是把播客发布工作压缩成一次高质量的编辑复核。它会尽量保留原话引用，标记不确定的说话人归属，并提示需要人工核查的事实、数据或敏感表述。
