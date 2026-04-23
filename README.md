# Skill Health Monitor 🏥

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Skill](https://img.shields.io/badge/Skill-Health_Monitor-orange.svg)]()

> **10+ skills? Rotting silently? Audit them before they fail you.**

## The Problem

Most AI agent operators accumulate 10-50 skills over time. Without maintenance:

| Symptom | Cause | Impact |
|---------|-------|--------|
| Skill never triggers | Outdated trigger phrases | Waste of context window |
| Agent gives bad advice | Skills conflict or overlap | Silent wrong behavior |
| No one finds your repo | Missing tags, vague description | 0 stars forever |
| Things break after updates | Dependency drift | Cascading failures |

**Real data:** The average [skill-doctor](https://github.com/xigua-wang/skill-doctor) scan finds 3-5 issues per skill collection. Unchecked, these compound into silent failures.

## The Solution

A **structured 5-dimension health scoring system** (0-100 points):

| Dimension | Weight | What It Checks |
|-----------|--------|---------------|
| 🏗️ **Structure** | 25% | File completeness (SKILL.md, README.md, LICENSE) |
| 📝 **Content** | 25% | Description quality, trigger phrases, examples |
| 🔄 **Activity** | 20% | Recent commits, version bumps, responsiveness |
| 🔗 **Compatibility** | 15% | Framework version alignment, breaking changes |
| 🔍 **Discoverability** | 15% | Tags, searchability, quick-start guide |

## Quick Start

```bash
# Install as an agent skill
# Claude Code: Copy SKILL.md to .claude/skills/skill-health-monitor/
# OpenClaw: Copy to ~/.openclaw/workspace/skills/skill-health-monitor/

# Then tell your agent:
"Run a health check on all my skills"
"Audit my skill collection"
"Which skills need attention?"
```

## Health Ratings

| Score | Rating | Action |
|-------|--------|--------|
| 90-100 | 🟢 Healthy | Maintain |
| 70-89  | 🟡 Needs Attention | Minor fixes (missing tags, vague description) |
| 50-69  | 🟠 Degrading | Schedule update (outdated patterns, missing files) |
| 0-49   | 🔴 Critical | Rewrite or retire |

## Sample Audit Output

```markdown
## Skill Health Report — 2026-04-24

### 🏥 Total: 12 skills audited

| Skill | Score | Status | Top Issue |
|-------|-------|--------|-----------|
| prompt-guard | 92 | 🟢 | None |
| token-budget | 85 | 🟡 | Missing GitHub topics |
| skill-xyz | 45 | 🔴 | No README, no LICENSE |
| ... | ... | ... | ... |

### Priority Actions
1. 🔴 Retire skill-xyz (score: 45) — missing critical files
2. 🟠 Update skill-old (score: 62) — outdated trigger phrases
3. 🟡 Add topics to token-budget — improve discoverability
```

## What Makes This Different

1. **Structured scoring** — Not "looks good to me" but a repeatable 100-point scale
2. **5 dimensions** — Catches surface issues (missing README) AND deep issues (outdated patterns)
3. **Action-oriented** — Every score comes with concrete next steps
4. **Collection-aware** — Designed for managing 10+ skills, not just one
5. **Trackable** — Diff reports show improvement or degradation over time

## Related Skills

- [**Code Audit**](https://github.com/aptratcn/skill-code-audit) — Audit your codebase quality
- [**MCP Security Audit**](https://github.com/aptratcn/skill-mcp-security-audit) — Audit MCP server security
- [**Quality Evaluator**](https://github.com/aptratcn/skill-quality-eval) — Evaluate agent output quality

## License

MIT

---

**Don't let your skills rot in silence. Audit early, audit often.**
