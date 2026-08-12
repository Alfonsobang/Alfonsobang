# Alfonsobang

I build public, reproducible evaluation infrastructure for financial research agents and LLM data quality.

Current focus: **A-share research quality, point-in-time financial search, backtest forensics, probabilistic forecasting, and Harbor-compatible agent tasks.**

[Open the A-Share Agent Arena](https://alfonsobang.github.io/open-market-eval/) | [Run point-in-time filing QA](https://alfonsobang.github.io/open-market-eval/filing-qa.html) | [Audit a backtest](https://alfonsobang.github.io/open-market-eval/#preflight) | [Audit research evidence](https://alfonsobang.github.io/open-market-eval/research-audit.html) | [中文说明](#中文简介)

[![OpenMarketEval A-Share Research Quality Gate](https://raw.githubusercontent.com/Alfonsobang/open-market-eval/main/docs/assets/open-market-eval-social-preview-v2.png)](https://alfonsobang.github.io/open-market-eval/)

## OpenMarketEval

[OpenMarketEval](https://github.com/Alfonsobang/open-market-eval) is an A-share research quality gate and public Agent arena. The project is deliberately built around inspectable contracts and deterministic failure tests rather than investment claims.

| Runnable surface | What it does | Public artifact |
| --- | --- | --- |
| Backtest Preflight | Checks eight A-share research-design risks locally or in CI | [Browser tool](https://alfonsobang.github.io/open-market-eval/#preflight) / [schema](https://github.com/Alfonsobang/open-market-eval/blob/main/schemas/backtest-contract.schema.json) |
| Research Evidence Audit | Checks six financial-search provenance failure classes without uploading the packet | [Browser tool](https://alfonsobang.github.io/open-market-eval/research-audit.html) / [method](https://github.com/Alfonsobang/open-market-eval/blob/main/docs/research-evidence-audit.md) |
| Point-in-Time Filing QA | Scores values, units, normalization, pages, and provenance on 10 facts from five official annual reports | [Browser lab](https://alfonsobang.github.io/open-market-eval/filing-qa.html) / [benchmark](https://github.com/Alfonsobang/open-market-eval/tree/main/benchmarks/a-share-point-in-time-qa) |
| Backtest Forensics | Scores any Agent on 10 adversarial A-share cases with clean controls | [challenge](https://github.com/Alfonsobang/open-market-eval/tree/main/benchmarks/a-share-backtest-forensics) |
| Harbor task pack | Packages forecasting, filing QA, backtest audit, and financial-search evidence as four schema 1.3 tasks | [tasks](https://github.com/Alfonsobang/open-market-eval/tree/main/integrations/harbor) |
| Live sealed forecasting | Commits predictions before resolution and scores calibration after outcomes | [current round](https://github.com/Alfonsobang/open-market-eval/tree/main/live/rounds/2026-08) |

```bash
git clone https://github.com/Alfonsobang/open-market-eval.git
cd open-market-eval
python -m open_market_eval doctor --output runs/doctor.json
python -m open_market_eval audit-research-packet \
  --packet examples/research-packets/leaky-packet.json \
  --output runs/research-audit.json
```

The `doctor` command verifies six bundled integrity paths offline, and CI publishes the JSON result as a downloadable artifact. The current public release is [`v0.7.0`](https://github.com/Alfonsobang/open-market-eval/tree/v0.7.0). Synthetic fixtures are labeled as fixtures; public leaderboards remain empty until independently reproducible submissions exist.

## Research Thesis

Financial Agents often fail outside ordinary Q&A benchmarks:

- evidence appears after the claimed research cutoff;
- citations exist but do not support the conclusion;
- current universes or revised fundamentals leak into historical tests;
- A-share T+1, suspension, and price-limit constraints are ignored;
- unstable tool trajectories are hidden behind fluent final answers.

My open-source work turns those failure modes into portable schemas, frozen fixtures, deterministic verifiers, scorecards, and review contracts.

## Other Public Work

- [Awesome LLM Training Data & Agent Evaluation](https://github.com/Alfonsobang/awesome-llm-training-data) - Bilingual resource hub and runnable finance-evaluation seed.
- [Financial RAG Evaluation Playbook](https://github.com/Alfonsobang/awesome-llm-training-data/blob/main/docs/financial-rag-evaluation-playbook.md) - Retrieval, citation, extraction, calculation, and refusal checks.
- [Financial Data Governance Control Plane](https://github.com/Alfonsobang/awesome-llm-training-data/blob/main/docs/financial-data-governance-control-plane.md) - Source manifests, cutoff rules, packaging policy, and redistribution boundaries.
- [Harbor/OpenCLAW trajectory audit](https://github.com/Alfonsobang/awesome-llm-training-data/tree/main/examples/harbor-openclaw-finance-trajectory-audit) - Synthetic finance-specific trace and safety audit.

## Upstream Discussions

- [harbor-framework/harbor#1700](https://github.com/harbor-framework/harbor/issues/1700) - Claw-style trajectory evaluation with repeated attempts and safety evidence.
- [huggingface/datatrove#485](https://github.com/huggingface/datatrove/issues/485) - Dataset-audit workflow with rejected-sample capture and machine-readable summaries.
- [argilla-io/argilla#5861](https://github.com/argilla-io/argilla/issues/5861) - Annotation QA workflow with suggestions, filters, and adjudication.

## Engineering Principles

- Prefer runnable artifacts over positioning claims.
- Prefer primary sources, point-in-time cutoffs, deterministic tests, and machine-checkable metadata.
- Publish misses and empty leaderboards honestly.
- Keep public examples free of private company data, real user data, proprietary workflows, investment advice, and trading signals.

## 中文简介

我关注金融研究 Agent 与 LLM 数据质量的可复现评测工程，当前重点是 A 股回测完整性、时点安全的金融搜索、证据引用、概率预测和 Harbor 任务。

目前的主项目是 [OpenMarketEval](https://github.com/Alfonsobang/open-market-eval)：它已经提供可在线运行的回测体检、研究证据审计和[年报时点查数实验室](https://alfonsobang.github.io/open-market-eval/filing-qa.html)，以及 10 个官方年报事实任务、10 个 A 股回测取证案例、4 个 Harbor schema 1.3 任务、六路径离线自检和带提交前封存与事后评分的预测闭环。

公开内容坚持使用公开来源、合成夹具、确定性检查和机器可读协议，不包含私有公司数据、真实用户数据、专有工作流、投资建议或交易信号。
