# humanizer-plugin

Cowork / Claude Code plugin wrapper around the [blader/humanizer](https://github.com/blader/humanizer) skill, which removes signs of AI-generated writing from text using the 29 patterns from Wikipedia's "Signs of AI writing" guide.

## What it does

Invoke `/humanizer` and paste text. The skill rewrites it to remove em-dash overuse, rule-of-three, sycophantic openers, vague attributions, and other AI tells. Optional voice calibration: paste 2-3 paragraphs of your own writing first to bias the rewrite toward your style.

## Layout

```
humanizer-plugin/
├── .claude-plugin/
│   └── plugin.json
├── skills/
│   └── humanizer/
│       └── SKILL.md
├── LICENSE
└── README.md
```

## Install

### Claude Code (CLI)

Push this folder to GitHub, then:

```bash
claude plugin marketplace add <your-gh-user>/humanizer-plugin
claude plugin install humanizer@humanizer-plugin
```

Or, for purely local use, the bare skill at `~/.claude/skills/humanizer/SKILL.md` already works without the plugin wrapper.

### Cowork

Push to GitHub, then install via the marketplace UI at https://claude.com/plugins (Customize > Browse plugins > install from URL).

## Credit

All skill content is from [blader/humanizer](https://github.com/blader/humanizer) (MIT licensed). This wrapper only adds the plugin manifest needed for Cowork distribution.
