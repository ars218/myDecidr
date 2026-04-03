# Design Reference

This document captures the visual language and design decisions behind Decidr, so the aesthetic stays consistent as the project evolves.

---

## Design Principles

1. **Calm over stimulating** — No loud colors, no gamification, no streaks. This is a thinking tool.
2. **Editorial over utilitarian** — Feels like opening a quality journal, not a task manager.
3. **Content over chrome** — UI elements stay out of the way. The user's words are the product.
4. **Mobile-native** — Designed for one hand, thumb-first, with proper safe area support.

---

## Color Palette

| Token | Value | Usage |
|---|---|---|
| `--bg` | `#0a0a0f` | App background |
| `--surface` | `#12121a` | Cards, panels |
| `--surface2` | `#1a1a26` | Input backgrounds, inner elements |
| `--text` | `#f0f0f0` | Primary text |
| `--text-muted` | `#8888aa` | Secondary text, labels |
| `--text-dim` | `#444460` | Placeholder, inactive elements |
| `--accent` | `#6366f1` | Indigo — CTAs, active states, highlights |
| `--accent-glow` | `rgba(99,102,241,0.35)` | Glow effects |
| `--accent-soft` | `rgba(99,102,241,0.12)` | Active chip backgrounds |

The palette is intentionally narrow. Indigo is the only hue. Everything else is near-black to near-white.

---

## Typography

| Role | Font | Weight | Size |
|---|---|---|---|
| Display / titles | Cormorant Garamond | 300–400 | 28–36px |
| Body | Outfit | 300 | 14–15px |
| Labels / eyebrows | Outfit | 500 | 10–12px |
| Metadata | Outfit | 300 | 12px |

**Why two fonts?** The serif (Cormorant) brings warmth and editorial weight to titles — the user's decision statement feels important when set in it. The sans (Outfit) handles everything functional at small sizes.

---

## Motion

- **View transitions**: 350ms, `cubic-bezier(0.4, 0, 0.2, 1)`, fade + 12px Y translate
- **Card press**: `scale(0.98)`, 200ms
- **Background orb**: 8s ease-in-out pulse, subtle scale 1→1.08
- **Toast**: 300ms slide-up, auto-dismiss at 2200ms

Motion is used sparingly. Every animation serves orientation or feedback — nothing decorative.

---

## Layout

- Max content width: unconstrained (full mobile width)
- Horizontal padding: 16–24px
- Bottom nav height: 64px + safe area inset
- Card border radius: 16px (`--radius`)
- Card border: `1px solid rgba(255,255,255,0.04)`

---

## Iconography

The app uses Unicode symbols and CSS-drawn elements rather than an icon library. This keeps the bundle size at zero and avoids external dependencies.

---

## Voice & Tone

- **Prompts are calm and non-judgmental** — "What did you decide?" not "Log your decision!"
- **Labels are lowercase when contextual** — feels personal, not corporate
- **Section labels use small-caps tracking** — creates hierarchy without loudness
