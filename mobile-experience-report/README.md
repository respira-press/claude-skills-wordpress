# Mobile Experience Report

**See what mobile visitors actually see** — broken layouts, oversized text, column stacking failures.

## What it does

Mobile Experience Report analyzes your WordPress site's responsive design using Respira for WordPress's MCP tools. It detects the layout issues that desktop testing misses, covering:

- **Breakpoint analysis** — tests all device sizes from 320px (iPhone SE) to 1024px (tablet landscape)
- **Column stacking failures** — multi-column layouts that squish side-by-side on phones
- **Typography scaling** — headings that eat the entire mobile screen
- **Horizontal scroll** — elements wider than the viewport causing sideways scrolling
- **Mobile navigation** — hamburger menu, tap targets ≥ 44px, touch-friendly dropdowns
- **Media responsiveness** — images, videos, maps without `max-width: 100%`
- **Spacing issues** — 80px desktop padding wasting the phone viewport
- **Mobile score** — 0–100 composite score with per-page breakdown and fix roadmap

## Requirements

- Respira for WordPress plugin (any version)
- Respira for WordPress MCP server connected to Claude
- WordPress 5.0+

## Installation

1. Install Respira for WordPress from [respira.press](https://www.respira.press)
2. Connect via MCP: `npx -y @respira/wordpress-mcp-server --setup`
3. Open Claude and say: `"audit mobile experience"`

## Trigger phrases

```
audit mobile experience
check mobile layout
mobile responsive issues
what do mobile users see
mobile design problems
responsive audit
my site looks bad on mobile
mobile layout broken
check responsive design
mobile ux audit
site broken on phones
```

## File structure

```
mobile-experience-report/
├── SKILL.md     ← Main skill definition (the actual skill prompt)
└── README.md    ← This file
```

## Telemetry

Anonymous usage data is sent to Respira after each run (site URL, WordPress/PHP versions, mobile score, issue counts, execution duration). No PII is collected. Telemetry is fire-and-forget — failures never affect skill output.

## Version history

### 1.0.0 (2026-03-07)
- Initial release
- Breakpoint analysis across all common device sizes
- Column stacking, typography, navigation, and media checks
- Mobile score calculation (0–100)
- Respira duplicate-first fix workflow recommendations
