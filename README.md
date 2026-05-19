# Project Summary Skill

Project Summary is a Codex skill that analyzes a repository or project and turns it into a resume-ready project story.

It is designed for Chinese and English resume workflows, especially when the user wants to package a project into:

- 项目背景
- 技术架构
- 个人职责
- 核心难点
- 解决方案
- 性能指标
- 可量化结果
- 面试可讲点

## What It Does

The skill first asks intake questions about the target role, personal ownership, deployment status, metrics, and desired output language. It then reads repository evidence and produces an honest project rewrite without inventing metrics or responsibilities.

## Install

Copy the skill folder into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R project-summary ~/.codex/skills/project-summary
```

Restart Codex to pick up the new skill.

## Usage

Example prompts:

```text
用 project-summary 分析这个仓库，帮我写成中文简历项目经历。
```

```text
Package this project for a backend engineer resume and prepare interview talking points.
```

## Structure

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
