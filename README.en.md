# Project Summary Skill

<p align="center">
  <a href="README.zh-CN.md"><img src="https://img.shields.io/badge/%E4%B8%AD%E6%96%87-%E4%BB%8B%E7%BB%8D-1677ff?style=for-the-badge" alt="中文介绍"></a>
  <a href="README.en.md"><img src="https://img.shields.io/badge/English-Introduction-111827?style=for-the-badge" alt="English introduction"></a>
</p>

Project Summary is a Codex skill that turns real repositories into resume-ready project stories, technical highlights, and interview talking points.

## When to Use

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

## How It Works

1. It asks a short intake question set before repository analysis.
2. It reads project evidence from README files, manifests, configs, tests, deployment files, and source directories.
3. It extracts architecture, engineering difficulty, implementation choices, and measurable outcomes.
4. It produces a structured project summary, resume bullets, and interview talking points.
5. Missing facts are listed as `待确认信息` instead of being invented.

## Install

```bash
mkdir -p ~/.codex/skills
cp -R project-summary ~/.codex/skills/project-summary
```

Restart Codex after installation.

## Example Prompts

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
