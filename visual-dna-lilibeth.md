# Visual DNA — Lilibeth's "Your Moodboard" deck

Source: `/Users/jasperstaats/Downloads/Your Moodboard.pdf` (Product Camp Design, Lilibeth Bustos Linares, 2025).

Captured 2026-05-11. Use as the editorial template for the foundation-arc slides in the Vibedesign Foundations workshop deck.

## Surface

| Token | Value | Use |
|---|---|---|
| `--lb-paper` | `#F0F0EE` | Page background. Warm off-white. Not pure. |
| `--lb-ink` | `#0A0A0A` | All type, all rules. |
| `--lb-acid` | `#D6FF5C` | The ONE accent. Title slide field, pill fills, highlight strokes. Use 1× per slide. |
| `--lb-hairline` | `#0A0A0A` | 1px solid rule under section tag, full bleed of left column. |
| `--lb-muted` | `#5A5A58` | Microcopy / caption color. |

No gradients. No tints. No shadows. Depth comes from hairlines and negative space.

## Type

- **ONE typeface** — geometric grotesque, condensed feel. PP Neue Montreal / GT Walsheim / Söhne family.
- **Weights:** 300 Light for display (DOMINANT), 400 Regular for microcopy, 500 Medium for pill text. Bold is forbidden.
- **Sizes — two only:** 140pt display, 16pt microcopy. No middle tier. The dominance gap is the design.
- **Letter-spacing:** -2% on display (`letter-spacing: -0.02em`). +12% on uppercase tags (`letter-spacing: 0.12em`).
- **Punctuation as design:** `¿…?` framing. Curly quotes. Em-dashes between ideas.
- **Line-height:** 1.0 on display (tight), 1.4 on microcopy.

## Grid

```
┌──────────────────────────────────────────────────────┐
│ TAG · 10pt UPPERCASE + 0.12em tracking               │  ← top-left, 56px from top
│ ──────────────────────────────────────────────────── │  ← 1px hairline, full bleed of left column
│                                                      │
│                                                      │
│ ¿Display                                             │
│  headline?                  [ RIGHT-SIDE IMAGE /     │
│                               COLLAGE / SPECIMEN     │
│                               full-bleed to right    │
│                               edge of slide ]        │
│                                                      │
│                                                      │
│                                                      │
│                                                      │
│                                                      │
│                                                      │
│ Microcopy caption ↓                                  │  ← bottom-left, 56px from bottom
└──────────────────────────────────────────────────────┘
```

- Slide split is roughly **45% left / 55% right** for content slides.
- Left column padding: 64px on all sides.
- Right column is FLUSH to the slide edge — image goes edge to edge.
- Microcopy sits at the **bottom of the left column**, never near the headline.

## Pills

```css
.lb-pill {
  display: inline-flex;
  align-items: center;
  padding: 8px 16px;
  border-radius: 999px;
  border: 1px solid var(--lb-ink);
  background: transparent;
  font-size: 10px;
  font-weight: 500;
  letter-spacing: 0.18em;
  text-transform: uppercase;
}
.lb-pill--filled { background: var(--lb-acid); border-color: transparent; }
.lb-pill--paper { background: var(--lb-paper); }
```

Used sparingly — title slide only on Lilibeth's deck. On content slides, the tag is just text + hairline.

## Reveal logic

The most original move: **same headline, different right-side answer** across 4–6 consecutive slides.

Slides 5–9 of the source deck all carry "¿Por qué es importante para tu portafolio?" but the right column changes each time:
1. (nothing — bare question)
2. Black-and-white portrait + caption "CLARIDAD"
3. Single white poster in a green field + caption "Evita el pánico de la página en blanco"
4. Collage with handwritten brand quote + caption "Te permite comunicar tu personalidad y estilo único."
5. Designer poster grid + caption "Sirve como guía práctica al elegir colores…"

It's narrative editing inside a deck. The headline is a **chorus**, the right-side is a **verse**.

## What's right, what's left

| Slot | Content |
|---|---|
| **Top-left** | Section tag (uppercase tracking, 10pt) + hairline rule |
| **Mid-left** | Display headline. Often a question. Light weight. Big. |
| **Bottom-left** | Microcopy caption. One sentence. The "punctuation" of the slide. |
| **Right column** | The visual answer. Always flush to slide edge. |

## Microcopy patterns

Bottom-left captions, all lowercase or sentence case, never bold:
- `CLARIDAD` (uppercase, 12pt) — when caption acts as a category label
- `Evita el "pánico de la página en blanco"` — when caption is a one-line teaching
- `Te permite comunicar tu personalidad y estilo único.` — when caption restates the headline's point

## Forbidden moves

- ❌ Gradients
- ❌ Drop shadows
- ❌ Bold weight
- ❌ More than 2 type sizes per slide
- ❌ More than 1 accent color
- ❌ Center-aligned text on content slides
- ❌ Imagery on the left while text is on the right (right-side imagery is the rule)
- ❌ Card backgrounds with fills (use hairlines or pure negative space)

## How to apply to the Vibedesign deck

| Vibedesign slide | Template adaptation |
|---|---|
| s1 Title | Optional B variant — acid-lime full bleed, black wordmark, two pills (top-left tag + bottom-right year) |
| s5 Diagnosis | Already 2-col. Strip card backgrounds, add hairline tag rule, move lede to bottom microcopy |
| s6 Voice | Manifesto cards collapse to a right-side poster stack of 3 quotes. Headline + microcopy on left. |
| s7 Colors | **First proof-of-concept.** Lilibeth treatment with palette specimens on the right. |
| s9 Type | "¿What does your typography sound like?" with type specimens on the right |
| s10 Layout | "¿How does your page breathe?" with grid+spacing diagram on the right |
| s12 References | Direct love letter to Lilibeth's slide 4. Editorial collage on the right. |
