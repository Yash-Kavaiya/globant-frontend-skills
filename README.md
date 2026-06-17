# Globant Frontend Design Skill

[![Hermes Agent](https://img.shields.io/badge/Hermes-Agent-blue)](https://hermes-agent.nousresearch.com)
[![Skill](https://img.shields.io/badge/Skill-globant--frontend--design-green)](https://hermes-agent.nousresearch.com/docs/skills)

A production-ready **Hermes Agent skill** for generating authentic Globant-branded frontend interfaces.

## Overview

This skill produces frontend UIs that look and feel like they belong to **Globant** — the visual system from their public brand portal (the **"Green Book"**).

### Signature Globant Aesthetic
- **White-predominant canvas** with calm, open layouts
- **Bright green gradient accents** (spring → mint → lime) as the signature flourish
- **Near-black text** (`#111`) for excellent readability
- **Bold, modern sans-serif** typography with generous tracking
- **Forward-pointing arrow motif** — Globant's recurring symbol of momentum
- **Delightful micro-interactions** aligned with *"technology that dares to delight"*

The skill intelligently chooses the right stack (React by default, or vanilla HTML/CSS) and faithfully applies the design system.

## Installation

### As a Hermes Skill

```bash
# Install directly from this repository
hermes skill install https://github.com/Yash-Kavaiya/globant-frontend-skills

# Or if you have the .skill file locally
hermes skill install ./globant-frontend-design.skill
```

### Manual Setup (for development)

1. Clone this repo
2. The `globant-frontend-design.skill` file is the ready-to-use packaged skill
3. `SKILL.md` contains the full skill definition and instructions

## Usage

Simply describe what you want built in Globant style:

```
"Create a modern landing page for a fintech product using Globant design"
"Build a dashboard with Globant green accents and clean white layout"
"Make this React component look like it's from Globant's Green Book"
```

The skill will:
1. Select the appropriate stack (React recommended)
2. Apply the complete design token system
3. Include signature elements: gradients, arrows, delightful motion
4. Ensure brand discipline (green as accent, never dominant)

## What's Included

- `SKILL.md` — Full skill definition and implementation guide
- `globant-frontend-design.skill` — Packaged distributable skill (includes references with design tokens, vanilla implementation, etc.)
- `README.md` — This file

The packaged `.skill` file contains:
- Complete design tokens (colors, gradients, typography, spacing, motion)
- Reference implementations for vanilla HTML/CSS and React
- Brand guidelines and quality checklist

## Design System Highlights

| Element | Globant Approach |
|---------|------------------|
| **Canvas** | White / near-white dominant |
| **Primary Accent** | Green gradients (only as highlights) |
| **Typography** | Bold display + clean body sans |
| **Motion** | Subtle forward-leaning interactions |
| **Icons/Motif** | Right-pointing arrows / chevrons |

## Contributing

This skill is designed to be extended. If you have access to Globant's internal brand assets or want to add new components, open an issue or PR.

## License

MIT — Feel free to use and adapt for your Globant-branded projects.

## Related

- [Hermes Agent Documentation](https://hermes-agent.nousresearch.com/docs)
- Globant Brand Portal (Green Book) — internal reference

---

**Built for Hermes Agent** • Part of the frontend skills ecosystem
