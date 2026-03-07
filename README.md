# Claude Skills for WordPress

**Open source Claude AI skills for WordPress developers and site owners.**

These skills work with [Respira for WordPress](https://www.respira.press) — a WordPress plugin that connects Claude AI to your site via MCP (Model Context Protocol). Each skill is a structured prompt that tells Claude exactly how to analyze or work with your WordPress installation.

---

## Available Skills

| Skill | Trigger | What it does |
|-------|---------|--------------|
| [WordPress Site DNA](./wordpress-site-dna/) | `"analyze my wordpress site"` | Full archaeological audit — builders, plugins, content, performance, security |
| [Technical Debt Audit](./technical-debt-audit/) | `"audit my wordpress technical debt"` | Orphaned shortcodes, unused plugins, database bloat, unused media |
| [WooCommerce Health Check](./woocommerce-health-check/) | `"check woocommerce health"` | Checkout issues, cart problems, payment gateways, mobile checkout |
| [Mobile Experience Report](./mobile-experience-report/) | `"audit mobile experience"` | Broken layouts, column stacking, typography, navigation on phones |

---

## How it works

1. **Install [Respira for WordPress](https://www.respira.press)** on your WordPress site
2. **Connect Claude** via the MCP server: `npx -y @respira/wordpress-mcp-server --setup`
3. **Say a trigger phrase** in Claude — the skill activates automatically

No configuration files to edit. No code to deploy. Just type a phrase and Claude runs the full audit.

---

## Requirements

- [Respira for WordPress](https://www.respira.press) plugin (free)
- Claude Desktop or Claude.ai with MCP support
- WordPress 5.0+

---

## What's a Skill?

Each skill is a `SKILL.md` file — a structured markdown document that Claude reads as instructions. It defines:

- Which trigger phrases activate it
- The step-by-step execution workflow
- Which MCP tools to call (and in what order)
- How to calculate scores and generate reports
- How to handle errors and partial failures
- Evaluation test cases for measuring accuracy

Skills are plain text. You can read them, modify them, or build your own.

---

## Skill structure

```
skill-name/
├── SKILL.md     ← The skill definition (what Claude reads)
└── README.md    ← Human-readable description and trigger phrases
```

Some skills include a `tests/` directory with benchmark, trigger tuning, and regression test cases.

---

## Contributing

Skills are open for community contributions. To propose a new skill or improve an existing one, open a pull request with a `SKILL.md` following the established format.

Good skill candidates:
- Repeatable WordPress audits with clear pass/fail criteria
- Tasks requiring multiple MCP tool calls in sequence
- Analysis that benefits from structured scoring and reporting

---

## Telemetry

Each skill sends anonymous usage data to Respira after running (site URL, WordPress/PHP versions, health score, issue counts, duration). No PII. Fire-and-forget — telemetry failures never affect skill output.

---

## License

MIT — see [LICENSE](./LICENSE)

Built by [Respira](https://www.respira.press)
