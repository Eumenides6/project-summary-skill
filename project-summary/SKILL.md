---
name: project-summary
description: Use when the user asks Codex to analyze a repository or project for a resume, portfolio, interview, 项目总结, 简历项目经历, 项目包装, 项目亮点, 面试项目介绍, architecture summary, or quantified project impact.
---

# Project Summary

## Overview

Turn a real project into an evidence-backed resume story. Read the project first, then rewrite it around architecture, ownership, difficulty, solution, measurable impact, and interview narratives.

## Workflow

1. Intake gate:
   - Before scanning files or drafting, first collect user context unless the user explicitly says to skip questions, "快速生成", "直接分析", or already provides enough context.
   - Ask up to 5 concise questions in one message. Prioritize target role/JD, personal ownership, deployment or usage status, real metrics, and desired output language/use case.
   - If the user answers partially, continue with their answers and put the remaining gaps in `待确认信息`.
   - If the user does not answer or asks to proceed without answers, continue from repository evidence and clearly state assumptions.

2. Identify the project type from source evidence:
   - Start with `rg --files`, `README*`, package manifests, lockfiles, Docker/CI/deploy files, config files, docs, tests, and top-level source directories.
   - Inspect only the files needed to understand architecture and user-facing behavior; avoid summarizing every file.
   - If there is git history, use it only for ownership or timeline clues when relevant.

3. Build an evidence map before writing:
   - Product: target users, problem, business or learning context.
   - Stack: language, framework, runtime, database, external APIs, deployment, tests, CI.
   - Architecture: modules, data flow, request flow, storage model, async jobs, integrations.
   - Difficulty: concurrency, scale, latency, reliability, security, UX complexity, data correctness, deployment constraints.
   - Results: measured numbers from docs/tests/benchmarks/logs, or clearly labeled estimate candidates.

4. Align the story to the target:
   - If a target role or JD exists, emphasize matching evidence: backend reliability, frontend UX, AI evaluation, data pipelines, full-stack delivery, or product impact.
   - If no target exists, default to software engineering or AI engineering based on the repository and state that assumption.

5. Rewrite with the required dimensions:
   - 项目背景
   - 技术架构
   - 个人职责
   - 核心难点
   - 解决方案
   - 性能指标
   - 可量化结果
   - 面试可讲点

6. Keep claims honest:
   - Do not invent metrics, users, revenue, ranking, latency, QPS, accuracy, or ownership.
   - Do not infer "I owned/built/led" from code existence alone; use the user's statement, commits, PRs, or mark responsibility as `待确认`.
   - If a useful metric is absent, write `待确认` or `可补充指标`, then suggest how to measure it.
   - Distinguish source-backed facts from reasonable inferences.

7. Produce resume-ready output:
   - Match the user's language. For Chinese resumes, use concise action verbs and result-first phrasing.
   - Prefer 3-5 bullets for a resume section, plus a fuller structured analysis when requested.
   - Make each bullet follow: action + technical method + difficulty/scale + result.
   - Remove filler such as "负责了很多", "参与开发", "提升用户体验" unless tied to concrete work or evidence.
   - End with `待确认信息` when missing facts would improve accuracy or impact.

## Reference

For formatting patterns, metric candidates, and interview prompts, read `references/resume-project-template.md`.
