# CraftCI (`io.github.srigenmedia/craft-ci`)

[![mcptry](https://mcptry.com/badge/io.github.srigenmedia/craft-ci)](https://mcptry.com/servers/io.github.srigenmedia/craft-ci)
[![CraftCI](https://craft.srigenmedia.com/badge/srigenmedia/craft-ci.svg)](https://craft.srigenmedia.com)

**Automated 20-Rule UX Craft, 5-Posture Playwright/Axe & Billing-Safety CI Gate + MCP Server (`https://craft.srigenmedia.com`)**

CraftCI catches AI-generated UI and billing regressions before production: horizontal overflow across 5 canonical viewports, WCAG 2.1 AA Axe violations, missing `401`/`403` auth gates, client-trusted pricing, missing HMAC webhook checks, and `>250` LOC bloat.

## Quickstart

### 1. Reusable GitHub Action

```yaml
- uses: srigenmedia/craft-ci@v0.1.0
  with:
    repo: "."
    min-score: "85"
```

### 2. Streamable HTTP MCP Client

```bash
claude mcp add --transport http craft-ci https://craft.srigenmedia.com/mcp
```

## MCP Tools

1. `craft_audit_code_snippet` — Full 20-rule static, UI posture, and billing-safety audit.
2. `craft_verify_billing_safety` — 5 critical Financial & Webhook Security rules (`401`/`403`, server SKU pricing, HMAC, idempotency, zero PII logs).
3. `craft_score_posture_report` — 10 layout and accessibility rules across 5 viewports.
4. `craft_generate_ci_gate` — Generates a ready-to-paste GitHub Actions workflow YAML.

Released under the [MIT License](LICENSE). See [SECURITY.md](SECURITY.md) for our fail-closed security policy.
