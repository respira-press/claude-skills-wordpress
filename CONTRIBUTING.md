# Contributing to Claude Skills for WordPress

Thanks for contributing. This repo is a community hub for practical WordPress skills that run inside Claude.

## What We Accept

- Skills that solve real WordPress problems on real sites
- Clear requirements and honest capability limits
- Safe workflows (read-only diagnostics or duplicate-first fixes)
- Reproducible output and actionable next steps

## Repository Structure

Each skill must live in `skills/` and follow Anthropic's official format:

- `skills/your-skill-name/SKILL.md` (required)
- `skills/your-skill-name/references/` (optional)
- `skills/your-skill-name/scripts/` (optional)

## Skill Quality Bar

- Tested on at least 3 real WordPress sites
- Trigger phrases and expected outputs documented
- Requirements explicit (plugin/add-on/version)
- No hardcoded credentials, endpoints, or secrets
- Language is specific, not vague or hype-driven

## Submission Process

1. Fork this repository
2. Create a branch for your skill
3. Add your `skills/your-skill-name/` folder
4. Open a PR using the PR template
5. Include anonymized example output and testing notes

### 1. Create Your Folder

```bash
mkdir -p skills/your-skill-name
cd skills/your-skill-name
touch SKILL.md
mkdir -p references
```

### 2. Create `SKILL.md` with YAML Frontmatter

```markdown
---
name: your-skill-name
description: What it does and when to use it. Use when user says [trigger phrases].
license: MIT
metadata:
  author: Your Name
  author_url: https://yoursite.com
  version: 1.0.0
  mcp-server: your-mcp-server
  category: audit
---

# Your Skill Name

[Main instructions - keep concise, under 5000 words]

For detailed examples, see `references/examples.md`
```

### 3. Move Detailed Content to `references/`

- `references/example-output.md` - detailed output examples
- `references/technical-details.md` - tool documentation
- `references/troubleshooting.md` - common issues

## Naming and Safety

- Use lowercase kebab-case folder names
- Prefer read-only diagnostics by default
- If fixes are included, enforce duplicate-first guardrails
- Call out destructive operations clearly

## Maintainer Review Criteria

- Real-world usefulness
- Accuracy and safety
- Clarity of docs and requirements
- Structural consistency with existing skills

## License

By submitting, you agree to license your contribution under MIT.
