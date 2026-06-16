# Ruel Belmonte

Backend engineer with 10+ years in C# / .NET, now building production AI
systems. I work where correctness and safety are the hard part: health-data
platforms, multi-tenant cloud infrastructure, and LLM tools whose guardrails are
enforced in code, not hoped for in a prompt.

## Currently building

- A consent-driven pipeline that pulls medical records from clinic systems
  (FHIR) and produces encrypted reports for NZ life insurers.
- Internal AI agents: Slack-native and retrieval-grounded, with every safety
  property (prompt-injection resistance, PII egress filtering, spend limits)
  enforced as tested code.
- Multi-tenant AWS infrastructure on EKS and Terraform, with per-customer data
  isolation.

## What I work with

- **Backend:** C# / .NET 10, ASP.NET Core, EF Core, PostgreSQL
- **AI:** RAG and agent systems, Anthropic API, guardrails and evals
- **Cloud / infra:** AWS, EKS, Terraform, GitHub Actions, OpenTelemetry
- **Frontend:** Vue 3, TypeScript

## Projects

Public repos, each small, tested, and CI-green, showing how I build rather than
just what I know:

- **[grounded](https://github.com/ruelbelmonte/grounded)** — a guardrailed RAG
  assistant for high-stakes domains: refusal-when-ungrounded, prompt-injection
  resistance, and PII egress filtering enforced as tested code. Python.
- **[resilient-ai](https://github.com/ruelbelmonte/resilient-ai)** — a
  production-grade .NET service for LLM-backed endpoints: Polly resilience,
  OpenTelemetry tracing with token/cost metrics, and Result-pattern error flow.
- **[mcp-notes](https://github.com/ruelbelmonte/mcp-notes)** — an MCP server
  exposing read-only, sandboxed tools over a notes vault, with a tested
  path-traversal boundary. TypeScript.
- **[vue-ai-chat](https://github.com/ruelbelmonte/vue-ai-chat)** — a Vue 3
  streaming chat UI done right: token streaming, cancellation, and error
  recovery as a tested state machine.
- **[promptproof](https://github.com/ruelbelmonte/promptproof)** — a red-team
  harness that tests whether an LLM system resists prompt injection, using
  deterministic canary-based leak detection. Python.
- **[keystone](https://github.com/ruelbelmonte/keystone)** — an enterprise-grade
  Clean Architecture / DDD `dotnet new` template: CQRS, EF Core, domain events,
  and architecture tests that enforce the layering. C# / .NET.

## Selected work

The rest lives in private repos, so the substance is described here rather than
linked. Happy to go deeper in conversation.

**Shirley, a guardrailed internal AI assistant.** A Slack-native assistant over
internal documentation. Prompt-injection resistance, PII egress filtering, and
confirm-before-write are enforced as tested code paths, not prompt requests.
Hybrid retrieval (semantic + keyword) feeds a bounded, read-only agent loop.
Python, FastAPI, Anthropic API, AWS App Runner.

## Get in touch

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ruelbelmonte)
