# Project Summary Skill / 项目总结 Skill

一个面向 Codex 的项目总结 Skill，用来把真实项目仓库整理成简历项目经历、技术亮点和面试讲稿。

Project Summary is a Codex skill that turns real repositories into resume-ready project stories, technical highlights, and interview talking points.

## 中文说明

### 适合什么场景

当你需要把一个项目写进简历、作品集或面试材料时，可以用这个 Skill 先读取项目证据，再生成更可信的项目描述。它会优先确认目标岗位、个人职责、上线情况、真实指标和你想要的输出语言，支持中文、英文、双语或其他指定语言，避免直接编造数据或把代码存在误写成个人贡献。

它会围绕这些维度重写项目：

- 项目背景
- 技术架构
- 个人职责
- 核心难点
- 解决方案
- 性能指标
- 可量化结果
- 面试可讲点

### 工作方式

1. 先提问收集关键信息，比如目标岗位、JD、个人职责、用户规模和真实性能指标。
2. 再读取仓库中的 README、依赖文件、配置、测试、部署文件和核心源码。
3. 根据证据提炼架构、难点、方案和结果。
4. 输出结构化项目总结、简历条目和面试可讲点。
5. 缺失或无法验证的信息会放进 `待确认信息`，不会伪造数字。

### 安装

```bash
mkdir -p ~/.codex/skills
cp -R project-summary ~/.codex/skills/project-summary
```

安装后重启 Codex，让新的 Skill 生效。

### 使用示例

```text
用 project-summary 分析这个仓库，帮我写成中文简历项目经历。
```

```text
这是一个面向后端实习的项目，请先问我必要信息，再帮我总结技术架构、难点和面试可讲点。
```

## English

### When To Use

Use this skill when you want to turn a repository into material for a resume, portfolio, or interview. The skill asks for the target role, JD, personal ownership, deployment status, real metrics, and your preferred output language before it analyzes the project. The output language is user-defined, including Chinese, English, bilingual output, or any other language you specify. It keeps unsupported claims out of the final text.

It rewrites a project around:

- Project background
- Technical architecture
- Personal contribution
- Core challenges
- Solutions
- Performance metrics
- Quantified results
- Interview talking points

### How It Works

1. It asks a short intake question set before repository analysis.
2. It reads project evidence from README files, manifests, configs, tests, deployment files, and source directories.
3. It extracts architecture, engineering difficulty, implementation choices, and measurable outcomes.
4. It produces a structured project summary, resume bullets, and interview talking points.
5. Missing facts are listed as `待确认信息` instead of being invented.

### Install

```bash
mkdir -p ~/.codex/skills
cp -R project-summary ~/.codex/skills/project-summary
```

Restart Codex after installation.

### Example Prompts

```text
Use project-summary to analyze this repository and write resume bullets for a backend engineer role.
```

```text
Package this project for an AI engineering interview. Ask me for missing context first.
```

## Repository Structure

```text
project-summary/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    └── resume-project-template.md
```

## License

MIT
