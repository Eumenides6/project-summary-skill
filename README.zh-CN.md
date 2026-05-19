# 项目总结 Skill

<p align="center">
  <a href="README.zh-CN.md"><img src="https://img.shields.io/badge/%E4%B8%AD%E6%96%87-%E4%BB%8B%E7%BB%8D-1677ff?style=for-the-badge" alt="中文介绍"></a>
  <a href="README.en.md"><img src="https://img.shields.io/badge/English-Introduction-111827?style=for-the-badge" alt="English introduction"></a>
</p>

一个面向 Codex 的项目总结 Skill，用来把真实项目仓库整理成简历项目经历、技术亮点和面试讲稿。

## 适合什么场景

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

## 工作方式

1. 先提问收集关键信息，比如目标岗位、JD、个人职责、用户规模和真实性能指标。
2. 再读取仓库中的 README、依赖文件、配置、测试、部署文件和核心源码。
3. 根据证据提炼架构、难点、方案和结果。
4. 输出结构化项目总结、简历条目和面试可讲点。
5. 缺失或无法验证的信息会放进 `待确认信息`，不会伪造数字。

## 安装

```bash
mkdir -p ~/.codex/skills
cp -R project-summary ~/.codex/skills/project-summary
```

安装后重启 Codex，让新的 Skill 生效。

## 使用示例

```text
用 project-summary 分析这个仓库，帮我写成中文简历项目经历。
```

```text
这是一个面向后端实习的项目，请先问我必要信息，再帮我总结技术架构、难点和面试可讲点。
```

## 仓库结构

```text
project-summary/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    └── resume-project-template.md
```

## 许可证

MIT
