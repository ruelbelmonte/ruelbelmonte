# Ruel Belmonte

Backend engineer with 10+ years in C# / .NET, now building production AI
systems. I work where correctness and safety are the hard part: health-data
platforms, multi-tenant cloud infrastructure, and LLM tools whose guardrails live
in tested code, not in a prompt.

## Currently building

- A consent-driven health-records integration (FHIR) that produces encrypted
  reports for downstream organisations.
- Internal retrieval-grounded AI agents. Their safety controls are code paths
  with tests, not prompt instructions: prompt-injection mitigation, PII egress
  filtering and spend limits.
- Multi-tenant AWS infrastructure on EKS and Terraform, with per-customer data
  isolation.

## What I work with

- **Backend:** C# / .NET 10, ASP.NET Core, EF Core, PostgreSQL
- **AI:** RAG and agent systems, Anthropic API, guardrails and evals
- **Cloud / infra:** AWS, EKS, Terraform, GitHub Actions, OpenTelemetry
- **Frontend:** Vue 3, TypeScript

## Featured: delivery security

Two public repos on how code gets from a pull request to production without
trusting more than it has to.

<a href="https://github.com/ruelbelmonte/secure-delivery-pipeline">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/ruelbelmonte/secure-delivery-pipeline/main/docs/images/secure-delivery-pipeline-dark.png">
    <img alt="secure-delivery-pipeline: build once, sign keylessly, verify before every deploy, promote the same digest to prod." src="https://raw.githubusercontent.com/ruelbelmonte/secure-delivery-pipeline/main/docs/images/secure-delivery-pipeline-light.png" width="100%">
  </picture>
</a>

**[secure-delivery-pipeline](https://github.com/ruelbelmonte/secure-delivery-pipeline)**:
a supply-chain-hardened CI/CD pipeline on GitHub Actions for a .NET 10 API. Images
are signed keylessly with cosign, carry an SBOM attestation, are verified before
every deploy, and are promoted to prod by digest without a rebuild. It runs end to
end on a free GitHub account, deploying to a throwaway kind cluster, with an
optional OIDC-authenticated Terraform stack for AWS.

<a href="https://github.com/ruelbelmonte/workflow-policy">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/ruelbelmonte/workflow-policy/master/docs/assets/workflow-policy-hero-dark.png">
    <img alt="workflow-policy: workflow files pass through seven rule probes; violations are pinpointed to file and line and reported as PR annotations and SARIF." src="https://raw.githubusercontent.com/ruelbelmonte/workflow-policy/master/docs/assets/workflow-policy-hero-light.png" width="100%">
  </picture>
</a>

**[workflow-policy](https://github.com/ruelbelmonte/workflow-policy)**: a GitHub
Action that lints workflows for least-privilege permissions and supply-chain
hygiene. Seven rules cover unpinned actions, unscoped write permissions,
`pull_request_target` misuse and script injection, and each violation fails CI
with a `file:line` annotation and SARIF for code scanning. It is static and makes
no network calls. Python.

## Projects

Public repos, each small, tested, and CI-green, showing how I build rather than
just what I know:

- **[grounded](https://github.com/ruelbelmonte/grounded)**: a guardrailed RAG
  assistant for high-stakes domains. It refuses when retrieval finds nothing,
  keeps retrieved context in escaped, delimited blocks, and redacts PII on the way
  out. Each guardrail is tested, and the README lists what each one misses.
  Python.
- **[resilient-ai](https://github.com/ruelbelmonte/resilient-ai)**: a .NET 10
  service for LLM-backed endpoints. It has layered Polly timeouts and retries that
  honour Retry-After, OpenTelemetry GenAI spans with token and cost metrics, and a
  Result-pattern error flow.
- **[mcp-notes](https://github.com/ruelbelmonte/mcp-notes)**: an MCP server
  exposing read-only, sandboxed tools over a notes vault. The path boundary is
  tested against traversal and symlink escapes, output is size-capped, and CI
  runs on Linux, Windows and macOS. TypeScript.
- **[vue-ai-chat](https://github.com/ruelbelmonte/vue-ai-chat)**: a Vue 3
  streaming chat UI. Token streaming, cancellation and error recovery are handled
  in a tested composable. [Live demo](https://ruelbelmonte.github.io/vue-ai-chat/),
  no API key needed.
- **[promptproof](https://github.com/ruelbelmonte/promptproof)**: a red-team
  harness that checks whether an LLM system leaks a planted canary under prompt
  injection. Detection is deterministic and catches encoded and look-alike
  leaks, and the CLI exits non-zero so it can gate CI. Python.
- **[keystone](https://github.com/ruelbelmonte/keystone)**: the `dotnet new`
  template I start services from. It is a .NET 10 minimal API with
  endpoint/service/validator/repository layers, a ServiceResult error flow,
  Dapper on Postgres, JWT scope policies and in-memory system tests. C# / .NET.

## Selected work

The rest lives in private repos, so the substance is described here rather than
linked. Happy to go deeper in conversation.

**A guardrailed internal AI assistant.** A chat-based assistant over internal
documentation. Prompt-injection mitigation, PII egress filtering and
confirm-before-write are implemented as tested code paths, not prompt
instructions. Hybrid retrieval (semantic + keyword) feeds a bounded, read-only
agent loop. Python, FastAPI, Anthropic API, AWS.

## Get in touch

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ruelbelmonte)
