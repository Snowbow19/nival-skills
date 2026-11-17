# Nival Skills

用于 UI 组件设计与交互式知识卡片制作的 Agent Skills。通过可运行的预览和反馈迭代，把设计方法变成可复用流程。

## Skills

| Skill | 用途 | 主要产出 |
| --- | --- | --- |
| [design-ui-components](skills/design-ui-components/SKILL.md) | 设计、改进按钮、开关、卡片、输入框与菜单；结合页面校准颜色、尺寸和状态 | 真实尺寸与放大细节的 HTML 预览、可编辑源码 |
| [build-interaction-reference-cards](skills/build-interaction-reference-cards/SKILL.md) | 把一个交互知识点整理成可体验的教学卡片 | 互动示例、术语、AI 指令、代表性使用场景 |

两者可以独立使用。前者关注组件本身；后者关注如何用卡片教会读者一种交互。没有固定配色、图标或场景，具体作品只出现在独立示例文件中。

## 安装

下载仓库 ZIP，或运行：

```sh
git clone https://github.com/Snowbow19/nival-skills.git
```

将 `skills/` 下需要的完整文件夹放进所用 Agent 支持的技能目录，保留 `SKILL.md`、`references/` 和 `agents/` 的相对位置。

Codex 的默认个人技能目录是 `~/.codex/skills/`。如果已经存在同名技能，先比较内容并备份，再决定是否替换。自定义了 `CODEX_HOME` 时，使用对应目录下的 `skills/`。

对于其他 Agent，按其技能加载方式导入完整文件夹；也可以让 Agent 阅读指定 `SKILL.md` 及它引用的文件。

## 使用

组件设计：

```text
使用 $design-ui-components，给这个页面设计一个开关。
先查看页面的背景、字体和相邻控件，提供真实尺寸和放大细节的 HTML 预览。
```

知识卡片：

```text
使用 $build-interaction-reference-cards，做一张讲解拖拽排序的知识卡片。
提供可操作的主示例、准确术语、一句可复用的 AI 指令，以及不同场景的小示例。
```

预览与公开发布分别遵循当前任务的授权。Skill 本身不授权修改或部署任何网站。

## 示例

- [书架导航交互](skills/design-ui-components/references/example-bookshelf.md)
- [页面配色校准](skills/design-ui-components/references/example-portfolio-colors.md)
- [手形指针、拖拽排序与行内校验卡片](skills/build-interaction-reference-cards/references/examples.md)
- [作品预览](https://nivalslibrary.com/portfolio)

示例中的精确尺寸、颜色、平台组合和数量不是通用默认值。概念演练与实际验证在示例中分别标明。

## 内容来源

技能方法来自 Nival 的组件与交互知识卡片设计实践。指针卡片示例的选题参考 [Adrian Punk 的鼠标指针文章](https://x.com/AdrianPunk115/status/2121882167290814692)。本仓库收录方法说明，不分发文章正文、系统指针资源或网站素材。

## 版本记录

见 [CHANGELOG.md](CHANGELOG.md)。
