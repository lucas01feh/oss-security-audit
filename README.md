# oss-security-audit

An agent skill that audits an open-source repository's supply chain security posture and produces an HTML report.

Methodology is based on [Astral's OSS security framework](https://astral.sh/blog/open-source-security-at-astral) (April 2026), covering:

1. CI/CD workflow security (triggers, action pinning, permissions, secret isolation)
2. Repository and organizational controls (branch/tag rulesets, 2FA, admin bypass)
3. Release security (Trusted Publishing, deployment environments, approvals, attestations, immutable releases)
4. Automations (GitHub Apps vs Actions for privileged triggers)
5. Dependency hygiene (automated updates, cooldowns, vuln surfacing, footprint)

Works against GitHub or GitLab. Read-only. The skill runs a preflight access check and asks the user to grant anything it's missing.

## Install

```
# Claude Code
git clone https://github.com/backnotprop/oss-security-audit ~/.claude/skills/oss-security-audit
```
```
# Codex
git clone https://github.com/backnotprop/oss-security-audit ~/.codex/skills/oss-security-audit
```
```
# Agents
git clone https://github.com/backnotprop/oss-security-audit ~/.agents/skills/oss-security-audit
```

## Use

In Claude Code, or any other agent, from inside the repo you want to audit:

> `/oss-security-audit`

The skill triggers, walks through the five domains, and writes `oss-security-audit-report.html` to the repo root.

## Layout

```
SKILL.md                    # methodology + workflow
assets/report-template.html # self-contained HTML report template
```

No bundled scanner. The audit is LLM-driven end to end.
