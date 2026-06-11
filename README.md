# 橙线插画 · Orange Line Illustration

**中文** | [English](README.en.md)

> 一个想法，一抹橙色，大量留白。
> One idea, one accent, lots of silence.

一套完整的插画风格系统（以 AI agent **skill** 的形式封装），用于生成纽约客风格的极简概念插画：纯白底上的细黑墨线、大量留白、唯一的暖橙点缀（`#F97316`），橙色永远落在意义所在的那个位置。

诞生于一次真实的工作流——为《与 AI 一起做产品的六条原则》绘制全套配图。

![封面示例](examples/cover-walking-through-the-draft.png)

## 里面有什么

- **风格规范** — 线条、底色、点缀色、人物、气质。让一整套图像出自同一个声音的那些规则。
- **隐喻设计方法** — 如何找到视觉张力，为什么动作场景胜过抽象符号（实战检验过，附失败案例）。
- **Prompt 模板** — 一套久经考验的骨架，适用于任何接受文字提示的生图模型。
- **字幕与标题系统** — 内页左下角安静的签名位，封面以标题为锚的版式。
- **抽卡工作流** — 生成便宜，AI 自检贵；批量出候选，让人来挑。

## 示例

| | |
|---|---|
| ![](examples/01-amplifier.png) | ![](examples/02-subtraction.png) |

注意尺度：人永远**极小**，物永远宏大。这种失衡感正是这个风格的签名式戏剧性。

## 安装

适用于任何支持 SKILL.md 约定的 AI agent（Cola、Claude Code、Codex 等）。把目录放进你的 agent 的 skill 文件夹即可，例如：

```
~/.cola/skills/orange-line-illustration/
```

然后直接对你的 agent 说——"给这篇文章配三张橙线风格插图"——它就会照着规范来。

## 协议

**双许可**：开源与个人使用免费；闭源/专有用途需购买商业授权。详见 [LICENSE.md](LICENSE.md)。
