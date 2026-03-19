# PIAdvisor Prompts

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

Official public system prompts and formatting templates for [PIAdvisor](https://piadvisor.net), the PixInsight assistant.

## Why This Repo Is Public

We open-sourced these prompts for a few simple reasons:

- **Transparency:** Users should be able to inspect the prompt logic behind PIAdvisor's guidance.
- **Community learning:** Advanced PixInsight workflows are hard-won. Sharing the prompt set helps others study, critique, and improve them.
- **Better contributions:** Prompt bugs, stale process advice, and missing edge cases are easier to fix when the source is public.

This repo is here to help the astrophotography community, not to hide the product's reasoning behind a black box.

## A Friendly Note On Reuse

The repository is MIT-licensed, so you can study it, fork it, and adapt it. We ask one thing in good faith: if this work helps your own project, please give PIAdvisor clear credit and do not repackage the prompt set as if it were written from scratch by someone else.

The goal is to share useful work with the community, not to make it easy to relabel the same prompt set as a different product.

## What Is In This Repo

```text
piadvisor-prompts/
├── prompts/
│   ├── system-prompt.md             # Public copy of the current shipped prompt
│   └── system-prompt-compressed.md  # Exact embedded compressed-form prompt shipped by the app
├── templates/
│   └── rich-formatting.md           # Markdown-to-UI formatting rules
├── CONTRIBUTING.md                  # Contribution guidelines
├── LICENSE                          # MIT License
└── README.md                        # This file
```

## Prompt Set Overview

### `prompts/system-prompt.md`

The public copy of PIAdvisor's current shipped system prompt. It is tuned for PixInsight 1.9.x, expects PIAdvisor's `flat_kv_v2` context snapshot, and covers:

- evidence-based diagnosis and workflow guidance
- adaptive explanations for beginner, intermediate, and advanced users
- OSC, LRGB, SHO/HOO, dual-band, and multi-image reasoning
- process ordering, failure recovery, and over-processing detection
- conversation-first behavior for both quick image shares and deeper review requests

### `prompts/system-prompt-compressed.md`

The exact compressed-form system prompt currently embedded in the shipped app. It is the most direct public reference when you want to compare repo prompt text with runtime behavior.

### `templates/rich-formatting.md`

Formatting rules for PIAdvisor's rich chat UI, including:

- callout boxes such as `Action`, `Warning`, and `Tip`
- tool links like `[[ProcessID]]`
- structure rules for headings, lists, and response layout

## How This Maps To The Shipped App

These prompts are not generic assistant prompts. They are written for PIAdvisor's runtime behavior and UI:

- the prompt expects a prepared PixInsight context snapshot, not raw free-form text
- image-aware turns may include current attachments plus older supporting visual context
- tool links rely on PIAdvisor's chat renderer
- some guidance assumes PIAdvisor-specific features such as context snapshots, visual memory limits, and rich response formatting

If you use these files outside PIAdvisor, expect to adapt the surrounding context format and UI behavior.

## Versioning

This repo tracks the latest shipped public PIAdvisor prompt set. For `1.2.0`, the embedded app prompt is the compressed-form prompt reflected here, and the rich formatting template is synced from the shipped default template used by the app. Users can still customize their local copies from the Settings panel.

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for the full workflow.

Good contributions include:

- correcting factual errors about PixInsight processes or scripts
- updating workflow guidance when PixInsight or popular plugins change
- clarifying edge cases, recovery paths, or diagnostic rules
- tightening prompt language without changing the technical intent

Out of scope:

- turning the prompt into a generic non-PixInsight assistant
- personality rewrites that weaken the technical, evidence-based tone
- large structural changes without discussion first

## Links

- **Website:** [https://piadvisor.net](https://piadvisor.net)
- **Public changelog:** [https://piadvisor.net/changelog/](https://piadvisor.net/changelog/)
- **Prompt repo issues:** [https://github.com/phatwila/piadvisor-prompts/issues](https://github.com/phatwila/piadvisor-prompts/issues)

## License

MIT License. See [LICENSE](LICENSE) for details.
