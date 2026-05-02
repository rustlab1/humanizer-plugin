# humanizer-plugin (Cowork marketplace)

A single-plugin Cowork marketplace that wraps the [blader/humanizer](https://github.com/blader/humanizer) skill.

## What's inside

One plugin: `humanizer` (see `./humanizer/`). It removes signs of AI-generated writing from text using the 29 patterns from Wikipedia's "Signs of AI writing" guide. Invoke with `/humanizer` and paste text; optional voice calibration if you paste a writing sample first.

## Layout

```
humanizer-plugin/
├── .claude-plugin/
│   └── marketplace.json     # lists the plugins in this marketplace
└── humanizer/
    ├── .claude-plugin/
    │   └── plugin.json      # plugin manifest
    ├── skills/
    │   └── humanizer/
    │       └── SKILL.md
    └── LICENSE
```

## Install

### Claude Code CLI

```bash
claude plugin marketplace add rustlab1/humanizer-plugin
claude plugin install humanizer@humanizer-plugin
```

### Cowork (desktop app)

Add this repo as a custom marketplace via the Directory UI, or register it manually in `~/Library/Application Support/Claude/.../cowork_plugins/known_marketplaces.json`.

## Credit

All skill content from [blader/humanizer](https://github.com/blader/humanizer) (MIT licensed). This repo only adds the marketplace + plugin manifests required for Cowork distribution.
