# Technical Debt Audit

**Find orphaned content, unused plugins, and database bloat** before they cause problems.

## What it does

Technical Debt Audit scans your WordPress installation for accumulated junk using Respira for WordPress's MCP tools. It covers:

- **Orphaned shortcodes** — shortcodes in content pointing to deleted or inactive plugins
- **Plugin graveyard** — installed but never activated, activated then abandoned
- **Builder archaeology** — dormant page builders with zero pages using them
- **Database bloat** — revisions, expired transients, orphaned postmeta, spam comments
- **Unused media** — images uploaded but referenced nowhere
- **Long inactive plugins** — deactivated 6+ months ago, still an attack surface
- **Debt score** — 0–100 composite cleanliness score with per-category breakdown
- **Safe cleanup roadmap** — prioritized week-by-week plan with Respira duplicate-first workflows

## Requirements

- Respira for WordPress plugin (any version)
- Respira for WordPress MCP server connected to Claude
- WordPress 5.0+

## Installation

1. Install Respira for WordPress from [respira.press](https://www.respira.press)
2. Connect via MCP: `npx -y @respira/wordpress-mcp-server --setup`
3. Open Claude and say: `"audit my wordpress technical debt"`

## Trigger phrases

```
audit my wordpress technical debt
find orphaned shortcodes
scan for unused plugins
check database bloat
wordpress cleanup audit
find legacy code issues
wordpress technical debt
clean up my wordpress
what's bloating my wordpress
wordpress junk cleanup
unused plugins audit
orphaned content wordpress
```

## File structure

```
technical-debt-audit/
├── SKILL.md     ← Main skill definition (the actual skill prompt)
└── README.md    ← This file
```

## Telemetry

Anonymous usage data is sent to Respira after each run (site URL, WordPress/PHP versions, debt score, issue counts, execution duration). No PII is collected. Telemetry is fire-and-forget — failures never affect skill output.

## Version history

### 1.0.0 (2026-03-07)
- Initial release
- Orphaned shortcode detection across all pages and posts
- Plugin categorization: never activated, activated-unused, long inactive
- Database bloat estimation
- Builder archaeology (installed vs actually used)
- Debt score calculation (0–100)
- Respira duplicate-first cleanup workflow recommendations
