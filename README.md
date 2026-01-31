# PIAdvisor Prompts

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

Official system prompts and formatting templates for [PIAdvisor](https://piadvisor.net).

## About

This repository contains the open-source system prompts that power PIAdvisor's reasoning engine. By open-sourcing these prompts, we aim to:

- **Transparency**: See exactly how PIAdvisor interprets your workspace
- **Community contributions**: Submit PRs to improve PixInsight-specific guidance
- **Best practices**: The prompts encode astrophotography processing workflows

## Repository Structure

```text
piadvisor-prompts/
├── prompts/
│   ├── system-prompt.md          # Main system prompt (full version)
│   └── system-prompt-compressed.md # Compressed version for token efficiency
├── templates/
│   └── rich-formatting.md        # UI formatting instructions
├── CONTRIBUTING.md               # How to contribute
├── LICENSE                       # MIT License
└── README.md                     # This file
```

## Prompt Overview

### System Prompt (`prompts/system-prompt.md`)

The main system prompt (~1000+ lines) that defines PIAdvisor's behavior:

- **Behavioral Core**: Evidence-based reasoning, adaptive explanation based on user expertise
- **Workflow Guidance**: Canonical processing order for OSC, LRGB, narrowband (SHO/HOO), and dual-band data
- **Prohibited Operations**: Rules that protect users from destructive workflow mistakes
- **Diagnostic Patterns**: Heuristics for detecting over-processing, halos, and calibration failures
- **Multi-Image Reasoning**: How to trace processing history across workspace images

### Rich Formatting Template (`templates/rich-formatting.md`)

Instructions for rendering responses in PIAdvisor's rich UI:

- Callout boxes (Action, Warning, Tip)
- Tool links (`[[ProcessID]]` syntax)
- Typography and structure guidelines

## Versioning

Prompts are versioned to match PIAdvisor releases. Each prompt file includes a version header:

```text
**Version:** 7.7
**Compatible with:** PIAdvisor 1.x
```

The shipped PIAdvisor module embeds a specific version of these prompts. Users can customize their local copy via the Settings panel.

## Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Good contributions:**

- Fixing factual errors about PixInsight processes
- Adding guidance for new tools (BlurXTerminator updates, new scripts)
- Clarifying workflow order or adding edge cases
- Improving diagnostic patterns based on real-world usage

**Not in scope:**

- Style/personality changes (keep the technical, evidence-based tone)
- Adding non-PixInsight topics
- Significant structural changes (discuss in an issue first)

## Usage Notes

These prompts are designed for PIAdvisor's specific context injection system. If you're adapting them for other purposes:

1. The prompts expect a **flat key-value context format** (documented in the prompt itself)
2. Tool links (`[[ProcessID]]`) require PIAdvisor's UI renderer
3. Some sections reference PIAdvisor-specific features (visual memory, history limits)

## Links

- **PIAdvisor Website**: [https://piadvisor.net](https://piadvisor.net)
- **PixInsight Forum Thread**: [Coming Soon]
- **Issue Tracker**: [GitHub Issues](../../issues)

## License

MIT License. See [LICENSE](LICENSE) for details.
