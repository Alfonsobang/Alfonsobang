# Alfonsobang

I work on AI training data and financial-agent evaluation: data quality, annotation systems, preference data, synthetic fixtures, data governance, trajectory-aware evaluation, and public-safe financial AI benchmarks.

My public work is intentionally conservative. It uses public sources, synthetic fixtures, deterministic checks, machine-checkable metadata, and reusable documentation. It does not use private company data, real user data, proprietary workflows, investment advice, or trading signals.

## Current Thesis

Financial agents often fail outside ordinary Q&A benchmarks:

- selecting the wrong source,
- mixing units, issuers, or reporting periods,
- citing evidence that does not support the answer,
- leaking post-cutoff information into forecasting tasks,
- producing personalized financial advice,
- and hiding unstable tool trajectories behind a fluent final answer.

I am building small, inspectable, public-safe evaluation assets for those failures.

## Main Project

[awesome-llm-training-data](https://github.com/Alfonsobang/awesome-llm-training-data) is being refocused from a broad LLM-data resource list into a practical portfolio for financial-agent evaluation and LLM data-quality engineering.

Start here:

- [Financial Agent Eval Seed](https://github.com/Alfonsobang/awesome-llm-training-data/tree/main/examples/financial-agent-eval-seed) - Runnable starter kit with 10 public-safe finance tasks, synthetic fixtures, Harbor-style templates, deterministic verifiers, known-bad examples, and generated reports.
- [Reference scorecard](https://github.com/Alfonsobang/awesome-llm-training-data/blob/main/examples/financial-agent-eval-seed/results/example-scorecard.md) - Generated scorecard for reference solutions.
- [Known-bad scorecard](https://github.com/Alfonsobang/awesome-llm-training-data/blob/main/examples/financial-agent-eval-seed/results/bad-finance-agent-scorecard.md) - Generated scorecard showing red flags across source, citation, numeric, temporal, tool-trajectory, and safety dimensions.
- [Scorecard builder](https://github.com/Alfonsobang/awesome-llm-training-data/blob/main/examples/financial-agent-eval-seed/build_scorecard.py) - Converts deterministic verifier reports into Markdown and JSON scorecards.
- [Task zoo](https://github.com/Alfonsobang/awesome-llm-training-data/blob/main/docs/financial-agent-evaluation-task-zoo.md) - Implemented and next task families for financial-agent evaluation.

One-command seed run:

```bash
python examples/financial-agent-eval-seed/run_finance_eval.py
```

Scorecard generation:

```bash
python examples/financial-agent-eval-seed/build_scorecard.py --report examples/financial-agent-eval-seed/results/example-report.json --candidate reference-solutions --output-prefix examples/financial-agent-eval-seed/results/example-scorecard
```

## Current Workstreams

- Financial-agent evaluation beyond static Q&A: public-source search, exact data lookup, filing-grounded QA, toy backtesting, cutoff discipline, risk calculation, tool-use traces, and compliance-boundary tasks.
- Harbor / OpenCLAW / ATIF-style trajectory auditing: repeated attempts, verifier evidence, tool traces, and process-safety checks.
- Financial RAG evaluation: retrieval, citation support, extraction, calculation, and refusal behavior.
- Financial evaluation data governance: source manifests, benchmark cards, synthetic-data labels, redistribution boundaries, and leakage controls.
- Annotation and preference-data quality for finance: evidence grounding, numeric correctness, safety boundaries, reviewer drift, and adjudication.

## Selected Public Artifacts

- [Project Pages Index](https://github.com/Alfonsobang/awesome-llm-training-data/blob/main/docs/README.md) - Guided map of the repo.
- [Financial Agent Evaluation Portfolio](https://github.com/Alfonsobang/awesome-llm-training-data/blob/main/docs/financial-agent-evaluation-portfolio.md) - Multi-entry strategy for runnable tasks, scorecards, governance, Harbor-style packaging, and positioning.
- [Financial Agent Evaluation Opportunity Map](https://github.com/Alfonsobang/awesome-llm-training-data/blob/main/docs/financial-agent-evaluation-opportunity-map.md) - Where the project can contribute without overclaiming.
- [Financial Agent Failure Gallery](https://github.com/Alfonsobang/awesome-llm-training-data/blob/main/docs/financial-agent-failure-gallery.md) - Failure modes that ordinary Q&A misses.
- [Financial RAG Evaluation Playbook](https://github.com/Alfonsobang/awesome-llm-training-data/blob/main/docs/financial-rag-evaluation-playbook.md) - Evaluation checks for finance RAG workflows.
- [Financial Data Governance Control Plane](https://github.com/Alfonsobang/awesome-llm-training-data/blob/main/docs/financial-data-governance-control-plane.md) - Source policy, packaging policy, cutoff, and redistribution controls.
- [Harbor Finance Task Pack Blueprint](https://github.com/Alfonsobang/awesome-llm-training-data/blob/main/docs/harbor-finance-task-pack-blueprint.md) - Public-safe task-pack shape for Harbor-style evaluation.
- [Harbor OpenCLAW financial ATIF trajectory audit](https://github.com/Alfonsobang/awesome-llm-training-data/tree/main/examples/harbor-openclaw-finance-trajectory-audit) - Synthetic trajectory audit with finance-specific safety and evidence checks.

## Upstream Discussions

- [harbor-framework/harbor#1700](https://github.com/harbor-framework/harbor/issues/1700) - Claw-style trajectory-aware evaluation pattern with repeated attempts and safety evidence.
- [huggingface/datatrove#485](https://github.com/huggingface/datatrove/issues/485) - Dataset-audit example using filters, rejected-sample capture, metadata, and summary stats.
- [argilla-io/argilla#5861](https://github.com/argilla-io/argilla/issues/5861) - Annotation QA workflow using guidelines, suggestions, filters, and adjudication.

## Open-source Principles

- Prefer runnable examples over claims.
- Prefer primary sources, deterministic tests, and machine-checkable metadata.
- Treat financial-domain AI evaluation as a governance and evidence problem, not a leaderboard race.
- Keep public examples free of private company data, real user data, proprietary workflows, investment advice, and trading signals.

## 中文简介

我关注 AI 训练数据与金融 Agent 评测工程，重点包括数据质量、标注系统、偏好数据、合成数据、数据治理、轨迹评测，以及公开安全的金融领域 AI 评测。

当前更明确的方向是：金融 Agent 的失败往往不在普通问答中暴露，而是在来源选择、数值单位、财务期间、未来数据泄漏、引用证据、合规边界和工具轨迹中暴露。

我正在把 [Awesome LLM Training Data & Agent Evaluation](https://github.com/Alfonsobang/awesome-llm-training-data) 从普通资料列表，重新聚焦为一个多入口的金融 AI 评测资产组合：可运行的 Financial Agent Eval Seed、金融 RAG 评测、数据治理、合成 fixture、标注与偏好质量、Harbor/OpenCLAW 风格轨迹审计，以及可生成的金融 Agent scorecard。

公开内容不包含私有公司数据、真实用户数据、专有工作流、投资建议或交易信号。
