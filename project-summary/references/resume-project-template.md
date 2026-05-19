# Resume Project Template

## User Intake

Default to asking intake questions before repository analysis. Skip only when the user explicitly asks for fast/no-question output, or has already provided enough context. Use at most 5 questions, then proceed with assumptions if the user does not answer.

Priority questions:

1. 目标岗位/JD 是什么？例如后端、前端、全栈、AI 工程师、算法、数据。
2. 你的个人职责是什么？独立完成、主导某模块、参与协作、负责优化，还是课程/开源项目？
3. 项目是否上线或被真实使用？用户量、数据量、请求量、生成量、部署环境是什么？
4. 有没有真实指标？例如延迟、准确率、通过率、成本、自动化节省时间、测试覆盖率。
5. 希望用什么输出语言？可以是中文、英文、双语，或任何用户指定的语言；用途偏校招、社招、实习、作品集，还是面试讲稿？

Opening message pattern:

```text
在分析项目之前，我先确认几个会显著影响简历表达的信息：
1. 目标岗位或 JD 是什么？
2. 你在这个项目里的个人职责是什么？
3. 项目是否上线或被真实使用？有没有用户量/数据量/请求量？
4. 有没有真实性能或业务指标？
5. 你希望用什么语言输出？中文、英文、双语或其他指定语言都可以；形式是简历版、作品集版，还是面试讲稿？
```

If the user gives a JD, map project evidence to JD keywords. If no role is provided, infer the strongest positioning from the repository and label it as an assumption.

## Evidence Table

Use this table internally before drafting.

| Dimension | Evidence to collect | If missing |
| --- | --- | --- |
| 项目背景 | README, docs, screenshots, product flows, domain names | Infer from code and mark as inference |
| 技术架构 | manifests, configs, source tree, Docker/CI, database schema | Describe observed architecture only |
| 个人职责 | user statement, commits, PRs, TODO ownership | Ask or mark `待确认` |
| 核心难点 | complex modules, retries, caching, auth, state sync, model logic, deployment | Name the likely engineering risk, not a vague "complexity" |
| 解决方案 | implementation paths, algorithms, middleware, state model, indexes, queues | Tie solution to specific files/modules |
| 性能指标 | benchmarks, logs, tests, bundle size, query count, response time | Suggest measurement method |
| 可量化结果 | before/after metrics, scale, coverage, latency, cost, conversion, automation time saved | Use `可补充指标` candidates |
| 面试可讲点 | tradeoffs, failures, alternatives, debugging stories | Turn architecture choices into questions |

## Output Structure

When the user wants a full project rewrite, use:

```markdown
## 项目名称

一句话定位：...

### 项目背景
...

### 技术架构
...

### 个人职责
...

### 核心难点
...

### 解决方案
...

### 性能指标
...

### 可量化结果
...

### 面试可讲点
1. ...
2. ...
3. ...

### 简历版项目描述
- ...
- ...
- ...

### 待确认信息
- 个人职责：...
- 真实性能/业务指标：...
- 上线状态/用户规模：...
- 可补充实验或测量方式：...
```

## Resume Bullet Pattern

Use compact bullets:

```text
基于 [技术栈/架构] 设计并实现 [核心能力]，解决 [难点]，实现/支撑 [量化结果或可验证结果]。
```

Good:

```text
基于 Next.js、PostgreSQL 与队列任务设计内容生成流水线，将长耗时 AI 任务拆分为异步状态机，支撑失败重试、进度追踪与结果持久化，降低用户等待中断风险。
```

Avoid:

```text
负责项目开发，使用多种技术提升了系统性能和用户体验。
```

## Metric Candidates

Prefer real measurements. If unavailable, propose these as `可补充指标`:

- Performance: P95 latency, cold start time, bundle size, render time, query time, throughput, memory usage.
- Reliability: retry success rate, error rate, failed job recovery, test pass rate, uptime.
- Productivity: manual steps removed, processing time saved, deployment time reduced, automated coverage.
- Product: active users, conversion rate, completion rate, retention, content generation volume.
- AI projects: accuracy, hallucination rate, evaluation pass rate, token cost, inference latency, human review time saved.

## Role Positioning

Adjust emphasis by target role:

| Target | Emphasize |
| --- | --- |
| 后端工程师 | API design, data model, concurrency, caching, queueing, reliability, observability, deployment |
| 前端工程师 | component architecture, state management, performance, accessibility, interaction complexity, design-system consistency |
| 全栈工程师 | end-to-end delivery, product flow, frontend/backend contracts, deployment, tradeoffs |
| AI 工程师 | model/API integration, prompt or RAG pipeline, evaluation, latency, token cost, safety guardrails |
| 数据/算法 | data pipeline, feature engineering, metrics, offline/online evaluation, correctness, scale |
| 产品/作品集 | user problem, MVP scope, iteration, adoption, measurable outcome |

## Interview Talking Points

Turn the project into 3-5 stories:

- Architecture choice: why this stack or module boundary, what alternatives were rejected.
- Hard bug: what failed, how it was diagnosed, what guardrail was added.
- Scale/performance: bottleneck, measurement method, optimization, tradeoff.
- Reliability/security: failure modes, auth/data safety, retries, validation, observability.
- Product judgment: user pain, MVP scope, what changed after feedback.

## Honesty Rules

- Replace unknown numbers with `待确认`, not fake precision.
- Use "支撑", "面向", "可扩展到" only when the architecture plausibly supports it; avoid claiming production scale without evidence.
- If personal responsibility is unknown, provide a neutral version and a user-fill version.
- Keep two versions when needed: `证据版` for fully supported claims, and `强化版` with clearly marked user-fill metrics.
