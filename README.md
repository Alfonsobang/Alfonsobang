# Hi, I'm Alfonsobang

I work on AI training data and financial agent evaluation, with a focus on LLM data quality, trajectory-aware evaluation, annotation systems, preference data, synthetic data, data governance, and financial-domain AI evaluation.

My public work is built from public sources, synthetic fixtures, deterministic checks, and reusable documentation. It does not rely on private company data, real user data, proprietary workflows, investment advice, or trading signals.

## Current Focus

- Financial agent evaluation beyond static Q&A: public-source search, exact data lookup, filing-grounded QA, toy backtesting, cutoff discipline, tool-use traces, and compliance-boundary tasks.
- FinAgentBench Seed: a small public-safe benchmark seed for financial agents that fail through source, unit, citation, cutoff, compliance, and trajectory errors.
- Harbor / OpenClaw / ATIF-style trajectory auditing, repeated-trial metrics, verifier evidence, and process-safety analysis.
- LLM training-data quality engineering, including cleaning, deduplication, inspection, annotation quality, preference data, synthetic data, and governance.

## Public Projects

- [awesome-llm-training-data](https://github.com/Alfonsobang/awesome-llm-training-data) - A bilingual hub that is being refocused from a broad resource list into a runnable financial agent evaluation seed.

## Current Public Work

- [Financial Agent Evaluation Positioning Thesis](https://github.com/Alfonsobang/awesome-llm-training-data/blob/main/docs/financial-agent-eval-positioning.md) - Why financial-agent evaluation should move from static Q&A to auditable tool-use evaluation.
- [FinAgentBench Seed Spec](https://github.com/Alfonsobang/awesome-llm-training-data/blob/main/docs/finagentbench-seed-spec.md) - Proposed benchmark shape for public-safe financial agent evaluation.
- [Financial Agent Eval Seed](https://github.com/Alfonsobang/awesome-llm-training-data/tree/main/examples/financial-agent-eval-seed) - Runnable starter kit with task specs, synthetic fixtures, Harbor-style templates, deterministic verifiers, source governance, known-bad examples, and generated reports.
- [Example financial eval report](https://github.com/Alfonsobang/awesome-llm-training-data/blob/main/examples/financial-agent-eval-seed/results/example-report.md) - Stable report generated from reference solutions.
- [Bad finance agent report](https://github.com/Alfonsobang/awesome-llm-training-data/blob/main/examples/financial-agent-eval-seed/results/bad-finance-agent-report.md) - Known-bad candidate report showing source, unit, citation, advice-boundary, and cutoff failures.
- [Harbor OpenClaw financial ATIF trajectory audit](https://github.com/Alfonsobang/awesome-llm-training-data/tree/main/examples/harbor-openclaw-finance-trajectory-audit) - Synthetic ATIF-v1.7 trajectory audit with finance-specific safety and evidence checks.

## Upstream Discussions

- [harbor-framework/harbor#1700](https://github.com/harbor-framework/harbor/issues/1700) - Claw-style trajectory-aware evaluation pattern with repeated attempts and safety evidence.
- [huggingface/datatrove#485](https://github.com/huggingface/datatrove/issues/485) - Dataset-audit example using filters, rejected-sample capture, metadata, and summary stats.
- [argilla-io/argilla#5861](https://github.com/argilla-io/argilla/issues/5861) - Annotation QA workflow using guidelines, suggestions, filters, and adjudication.

## Open-source Principles

- Prefer runnable examples over claims.
- Prefer primary sources, public documentation, deterministic tests, and machine-checkable metadata.
- Treat financial-domain AI evaluation as a governance and evidence problem, not a leaderboard race.
- Avoid private company data, real user data, proprietary workflows, investment advice, and trading signals.

## 中文简介

我关注 AI 训练数据与金融 Agent 评测工程。当前更明确的方向是：金融 Agent 的失败往往不在普通问答里暴露，而是在来源选择、数值单位、财务期间、未来数据泄漏、引用证据、合规边界和工具轨迹中暴露。

我正在把 [Awesome LLM Training Data & Agent Evaluation](https://github.com/Alfonsobang/awesome-llm-training-data) 从普通资料列表，重新聚焦为一个公开安全、可运行、可审计的金融 Agent 评测 seed。这个方向暂称为 FinAgentBench Seed。

公开内容不包含私有公司数据、真实用户数据、专有工作流、投资建议或交易信号。
