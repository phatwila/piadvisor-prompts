# Contributing to PIAdvisor Prompts

Thank you for your interest in improving PIAdvisor! This document explains how to contribute effectively.

## Before You Start

1. **Read the existing prompts** to understand the structure and style
2. **Check existing issues** to see if your idea has been discussed
3. **Open an issue first** for significant changes. Get feedback before investing time.

## Types of Contributions

### ✅ Welcome

- **Factual corrections**: Process behaves differently than described
- **Missing edge cases**: "What about when X happens?"
- **New tool guidance**: Support for new processes or scripts
- **Diagnostic improvements**: Better heuristics for common problems
- **Clarity improvements**: Rewording confusing sections
- **Typo/grammar fixes**: Always appreciated

### ⚠️ Discuss First

- **Structural changes**: Reorganizing sections or changing format
- **New major sections**: Adding entirely new topic areas
- **Behavioral changes**: Changing how PIAdvisor reasons or responds

### ❌ Out of Scope

- Personality or style changes (keep the technical, evidence-based tone)
- Non-PixInsight topics
- Marketing language or promotional content
- Changes that would make prompts vendor-specific

## Pull Request Process

### 1. Fork and Clone

```bash
git clone https://github.com/YOUR-USERNAME/piadvisor-prompts.git
cd piadvisor-prompts
```

### 2. Create a Branch

```bash
git checkout -b fix/spcc-white-reference-clarity
```

Use descriptive branch names:

- `fix/` for corrections
- `feat/` for new guidance
- `docs/` for documentation improvements

### 3. Make Your Changes

- Keep changes focused. One logical change per PR.
- Maintain existing formatting style
- Test your changes if possible (see below)

### 4. Commit with Clear Messages

```bash
git commit -m "Fix: Clarify SPCC White Reference selection guidance

- Add G2V Star vs Average Spiral Galaxy decision tree
- Include common failure mode for galaxy-dominant fields
- Reference real-world example from M33 processing"
```

### 5. Open a Pull Request

Include:

- **What** you changed
- **Why** you changed it
- **How** you tested it (if applicable)

## Testing Your Changes

If you have PIAdvisor installed:

1. Copy your modified prompt to your PIAdvisor config directory:
   - Windows: `%APPDATA%\PixInsight\PIAdvisor\system-prompt.txt`
   - macOS: `~/Library/Application Support/PixInsight/PIAdvisor/system-prompt.txt`

2. Restart PIAdvisor or use the "Reset" button in Settings

3. Test relevant scenarios with your changes

## Style Guide

### Formatting

- Use **bold** for process names: `**DynamicCrop**`
- Use `backticks` for parameters, filenames, and code: `fits.FILTER`
- Use headers to organize: `### Section`, `#### Subsection`
- Use tables for structured comparisons
- Use blockquotes for callouts: `> **Action:** Do this now`

### Tone

- **Technical but accessible**: Explain complex concepts clearly
- **Evidence-based**: Reference specific context keys or visual evidence
- **Prescriptive when needed**: Clear guidance, not wishy-washy suggestions
- **Adaptive**: Acknowledge different skill levels and use cases

### Rules

- Never add marketing language
- Never suggest processes that don't exist in PixInsight
- Never provide advice that could damage user data without explicit warnings
- Always cite the evidence source (history, statistics, visual, etc.)

## Prompt Structure

The system prompt follows this structure:

1. **Introduction**: Role and philosophy
2. **Behavioral Core**: Reasoning principles
3. **Evidence Hierarchy**: How to weight different context sources
4. **State Detection**: Linear vs stretched, data types
5. **Workflow Master Keys**: Canonical processing order
6. **Advanced Analysis**: Specialized diagnostic branches
7. **Rich UI Guidelines**: Formatting for PIAdvisor's interface

When adding content, place it in the appropriate section. Don't add new top-level sections without discussion.

## Questions?

- **General questions**: Open a Discussion
- **Bug reports**: Open an Issue
- **Feature requests**: Open an Issue with `[Feature Request]` prefix

---

Thank you for helping make PIAdvisor better! 🔭
