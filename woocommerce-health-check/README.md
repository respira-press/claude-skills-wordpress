# WooCommerce Health Check

**Detect checkout issues, cart problems, and configuration errors** silently losing sales.

## What it does

WooCommerce Health Check scans your store for common configuration issues that break checkout flow using Respira for WordPress's MCP tools. It covers:

- **URL mismatch detection** — WordPress Address vs Site Address mismatch breaks AJAX on checkout
- **SSL verification** — HTTP store means payment gateways won't process
- **Cart & checkout pages** — verifies pages exist, are published, and correctly assigned in WooCommerce settings
- **Caching exclusions** — cart/checkout cached = sessions broken, empty carts, lost orders
- **Payment gateways** — detects active gateways, flags inactive plugins, SSL requirements
- **Mobile checkout** — column stacking, tap targets, Place Order button off-screen
- **Checkout performance** — load time, unnecessary scripts, JS blocking payment forms
- **Health score** — 0–100 store-specific score with immediate actions sorted by revenue impact

## Requirements

- Respira for WordPress plugin (any version)
- Respira for WordPress MCP server connected to Claude
- WordPress 5.0+
- WooCommerce installed and active

## Installation

1. Install Respira for WordPress from [respira.press](https://www.respira.press)
2. Connect via MCP: `npx -y @respira/wordpress-mcp-server --setup`
3. Open Claude and say: `"check woocommerce health"`

## Trigger phrases

```
audit my woocommerce store
check woocommerce health
find checkout problems
woocommerce diagnostic
why is my checkout broken
scan woocommerce configuration
woocommerce health check
checkout not working woocommerce
cart problems woocommerce
woocommerce checkout issues
losing sales woocommerce
woocommerce configuration audit
```

## File structure

```
woocommerce-health-check/
├── SKILL.md     ← Main skill definition (the actual skill prompt)
└── README.md    ← This file
```

## Telemetry

Anonymous usage data is sent to Respira after each run (site URL, WordPress/PHP versions, health score, issue counts, execution duration). No PII is collected. Telemetry is fire-and-forget — failures never affect skill output.

## Version history

### 1.0.0 (2026-03-07)
- Initial release
- URL mismatch and SSL detection
- Cart/checkout page configuration checks
- Caching plugin exclusion verification
- Payment gateway status detection
- Mobile checkout experience analysis
- Checkout performance profiling
- Health score calculation (0–100)
- Respira duplicate-first fix workflow recommendations
