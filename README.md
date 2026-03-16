# Claude Skills for WordPress

The community hub for WordPress AI workflows.

Skills that run inside Claude, Codex, Cursor, and any AI agent that supports Skills + MCP to analyze, audit, optimize, and fix WordPress sites.  
Built by the community. Curated by Respira. Open source.

**Live Directory:** https://www.respira.press/skills

---

## What Are Skills?

Skills teach AI agents how to work with WordPress in ways that respect your site's architecture and your need for control.

**Plain AI agent:** Generic guidance based on best practices  
**Respira-powered skills:** Deep site access via 103+ MCP tools

---

## Available Skills

### Onboarding

**[Site Onboarding](skills/site-onboarding)**  
First-run primer: verifies MCP connection, discovers site architecture, maps all capabilities, recommends marketplace skills.  
*By Respira for WordPress*

### Audit Skills

**[WordPress Site DNA](skills/wordpress-site-dna)**  
Comprehensive site archaeology: builders, plugins, content structure, technical debt.  
*By Respira for WordPress*

**[Technical Debt Audit](skills/technical-debt-audit)**  
Finds orphaned shortcodes, unused plugins, database bloat, inactive builder data.  
*By Respira for WordPress*

**[WooCommerce Health Check](skills/woocommerce-health-check)**  
Store diagnostics: checkout issues, cart problems, payment gateway configuration.  
*By Respira for WordPress* · Requires WooCommerce add-on

**[Mobile Experience Report](skills/mobile-experience-report)**  
Mobile layout analysis: responsive breakpoints, touch targets, navigation issues.  
*By Respira for WordPress*

### Performance Skills

**[SEO & AEO Amplifier](skills/seo-aeo-amplifier)**  
On-page SEO and Answer Engine Optimization with automated schema generation.  
*By Respira for WordPress*

**[WordPress AI Image Optimizer](skills/wordpress-ai-image-optimizer)**  
AI-powered image optimization: compress, convert to WebP, resize, rename, alt text, and update references.  
*By Respira for WordPress*

**[Internal Link Builder](skills/internal-link-builder)**  
Strategic internal link building: scans content, maps topic relationships, finds linking opportunities, applies with duplicate-first safety.  
*By Respira for WordPress*

### Migration Skills

**[Content Portability](skills/content-portability)**  
Export WordPress content to portable local packages with builder data, media, and markdown previews. Import to another site with smart ID remapping. Auto-backup before AI edits. Diff local exports against live site.  
*By Respira for WordPress*

---

## Skill Structure

Each skill follows Anthropic's official format:

````
skills/skill-name/
├── SKILL.md (with YAML frontmatter - main instructions)
├── references/ (optional - detailed docs)
│   ├── example-output.md
│   └── technical-details.md
└── scripts/ (optional - executable code)
````

**No README.md or metadata.json inside skill folders** - all documentation goes in SKILL.md or references/

---

## Contributing

**We want skills that solve real problems on real WordPress sites.**

See [CONTRIBUTING.md](CONTRIBUTING.md) for:
- How to submit a skill
- Quality standards
- Skill structure requirements
- Recognition and rewards

**Quick start:**
1. Fork this repo
2. Create your skill in `skills/your-skill-name/`
3. Include SKILL.md with YAML frontmatter
4. Test on 3+ real WordPress sites
5. Submit PR

[Read Full Guidelines →](CONTRIBUTING.md)

---

## Recognition

Accepted skills get:
- Featured in https://respira.press/skills directory
- Author attribution with link to your site/GitHub
- Usage stats shared monthly
- Promotion in newsletter and social channels
- Your name in contributors list

---

## Support

**Questions?**
- Issues: [GitHub Issues](https://github.com/webmyc/claude-skills-wordpress/issues)
- Discord: [Join Respira Discord](https://go.respira.cafe/respira-discord)
- Email: word@respira.press

**Found a bug in a skill?**  
Open an issue with the skill name in the title.

**Want to improve a skill?**  
Fork, improve, submit PR. Tag original author if possible.

---

## License

All skills are MIT licensed. By contributing, you agree to license your skill under MIT.

---

## Directory

Browse all skills: https://www.respira.press/skills

Built by the WordPress community. Curated by Respira for WordPress.
