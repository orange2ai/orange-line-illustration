# 橙线插画 · Orange Line Illustration

**中文** | [English](README.en.md)

> 一个想法，一抹橙色，大量留白。
> One idea, one accent, lots of silence.

一套完整的插画风格系统（以 AI agent **skill** 的形式封装），用于生成纽约客风格的极简概念插画：纯白底上的细黑墨线、大量留白、唯一的暖橙点缀（`#F97316`），橙色永远落在意义所在的那个位置。

支持两种工作流：
- **单张插图** — 为文章、原则、封面生成概念配图
- **PPT 演讲稿** — 将文章/大纲变成带插图的 HTML 幻灯片

![封面示例](examples/cover-walking-through-the-draft.png)

---

## 角色 IP 系统

这套风格有三个可复用的角色 IP，每个都有固定的形态和性格定义。

### 小橙（默认角色）

纯黑线条勾勒的几何小人，胸口一个橙色圆点。安静做事，不声张。

- 圆形头部（轮廓不填色）+ 两个黑点眼 + 无嘴
- 窄长方形身体轮廓 + 细线四肢
- 胸口唯一的橙色圆点 `#F97316` = 整张图的点缀色
- 必须参与核心动作，不能只是装饰

| 信息爆炸 | 事找人 |
|---|---|
| ![](examples/xiaocheng-info-overload.png) | ![](examples/xiaocheng-tasks-find-you.png) |

### 线人

极简抽象人形——圆形头部 + 一根弧线身体 + 单线四肢。最少的笔画构成"有人在这里"。

| 雨燕不落地 |
|---|
| ![](examples/xianren-swift-never-lands.png) |

### 线猫

10-12 笔画完的幼猫符号——不闭合的弧线、两个黑点眼、两撇耳朵。观者的大脑自动补全。

| 薛定谔的用户 |
|---|
| ![](examples/xianmao-schrodinger-user.png) |

---

## 风格规范（快速一览）

- **线条**：细黑墨线，手绘微抖，不机械
- **背景**：纯白，不要纸纹、渐变、阴影
- **点缀色**：唯一暖橙 `#F97316`，落在最有意义的那个元素上
- **人物**：极小。物永远宏大，人永远渺小，这种失衡感是签名式戏剧性
- **气质**：witty, restrained, intelligent

详见 `SKILL.md` 和 `references/` 目录下的完整规范。

---

## 两种工作流

### 工作流 A：单张概念插图

为文章中的某个判断、原则、隐喻生成一张 16:9 配图。

```
给这篇文章配三张橙线风格插图
```

流程：提炼隐喻 → 设计场景 → 生成候选 → 人来挑选

### 工作流 B：PPT 演讲稿

将文章/大纲变成带插图的 HTML 幻灯片，每页一张场景插画。

```
把这篇文章做成橙线 PPT
```

流程：读文章 → 写幻灯片大纲 → 确认 → 批量生成插图 → 用户选图 → 输出 HTML

详见 `references/ppt-workflow.md`。

---

## 里面有什么

```
.
├── SKILL.md                          # 主规范：风格、隐喻方法、prompt 模板
├── references/
│   ├── xiao-orange-ip.md             # 小橙 IP 定义
│   ├── xiao-orange-prompt-template.md # 小橙生图模板
│   ├── xianren-ip.md                 # 线人 IP 定义
│   ├── xianmao-ip.md                 # 线猫 IP 定义
│   └── ppt-workflow.md               # PPT 演讲稿工作流
├── examples/                         # 示例图片
├── LICENSE.md
└── README.md
```

## 安装

适用于任何支持 SKILL.md 约定的 AI agent（Cola、Claude Code、Codex 等）。把目录放进你的 agent 的 skill 文件夹即可：

```bash
# Cola
~/.cola/skills/orange-line-illustration/

# Claude Code
~/.claude/skills/orange-line-illustration/
```

然后直接对你的 agent 说——"给这篇文章配三张橙线风格插图"或"把这篇文章做成橙线 PPT"——它就会照着规范来。

## 协议

**双许可**：开源与个人使用免费；闭源/专有用途需购买商业授权。详见 [LICENSE.md](LICENSE.md)。
