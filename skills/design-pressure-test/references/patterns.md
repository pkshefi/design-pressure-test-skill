# Design Pressure Test — Spacing Patterns

## Hero Section

### Single-CTA Hero
```
┌──────────────────────────────────────┐  ← pt-20 (80px) to pt-24 (96px)
│                                      │
│          Headline (mb-4)             │
│          Subheadline (mb-8)          │
│          [CTA Button]                │
│          Trust signals (mt-10)       │
│                                      │
├──────────────────────────────────────┤
│         Next Section                 │
└──────────────────────────────────────┘  ← pb-16 (64px) to pb-24 (96px)
```

### Split Hero (image + text)
```
┌──────────┬───────────────────────────┐
│          │                           │
│  Text    │       Image               │
│  Col     │       Col                 │
│  pt-20   │                           │
│          │                           │
│          │                           │
├──────────┴───────────────────────────┤
│         Next Section                 │
└──────────────────────────────────────┘
```
- Gap between columns: `gap-12` (48px) to `gap-16` (64px)
- Text max-width: 480–560px

## Card Patterns

### Testimonial Card
```
┌──────────────────────────────────┐
│  ═══ (p-10 to p-12) ═══         │  ← 40–48px all sides
│  ★★★★★                           │
│                                  │
│  "Quote text that wraps to       │
│   multiple lines and needs       │
│   comfortable breathing."        │
│                                  │
│  — Author Name, Title            │
│  ═════════════════════════════   │
└──────────────────────────────────┘
```

### Pricing Card
```
┌──────────────────────────────────┐
│  ═══ (p-10 to p-12) ═══         │  ← 40–48px all sides
│                                  │
│  Plan Name    (mb-2)             │
│  $49/mo       (mb-6)             │
│                                  │
│  ✓ Feature 1   (gap-3)           │  ← 12px between items
│  ✓ Feature 2                     │
│  ✓ Feature 3                     │
│  ✓ Feature 4                     │
│                                  │
│  [CTA Button]   (mt-8)           │
│  ═════════════════════════════   │
└──────────────────────────────────┘
```

### Feature Card (grid layout)
```
┌───────────────────────┐
│  ═══ (p-8 to p-10) ═══│  ← 32–40px all sides
│                       │
│  🔥 Icon   (mb-4)     │
│  Title     (mb-2)     │
│  Description text     │
│  that wraps...        │
│                       │
└───────────────────────┘
```
- Grid gap between cards: `gap-6` (24px) to `gap-8` (32px)

## Form Patterns

### Single-Column Form
```
┌──────────────────────────────────┐
│  ═══════ (p-8 to p-10) ═══════  │
│                                  │
│  Label          (mb-1)           │  ← 4px label to input
│  [Input Field]  (mb-5)           │  ← 20px between fields
│  Label          (mb-1)           │
│  [Input Field]  (mb-5)           │
│  Label          (mb-1)           │
│  [Input Field]  (mb-5)           │
│                                  │
│  [Submit Button]   (mt-2)        │
│  ═════════════════════════════   │
└──────────────────────────────────┘
```
- Input inner padding: `px-4 py-3` (16px horizontal, 12px vertical)
- Submit button: `px-8 py-4` (32px horizontal, 16px vertical)

## CTA Section Patterns

### Full-Width CTA
```
┌──────────────────────────────────────┐  ← pt-16 pb-16 to pt-20 pb-20
│                                      │
│      Headline (mb-4)                 │
│      Subheadline or description      │
│      (mb-8)                          │
│                                      │
│   [Primary]  [Secondary]  (gap-4)    │  ← 16px between buttons
│                                      │
│      Trust line (mt-8)               │
│                                      │
└──────────────────────────────────────┘  ← pt-16 pb-16 to pt-20 pb-20
```

## Navigation Patterns

### Landing Page Nav (minimal)
```
┌──────────────────────────────────────┐
│  [Logo]              [CTA Button]    │  ← py-4 (16px vertical)
│                                      │  ← px-6 (24px horizontal)
└──────────────────────────────────────┘
```
- Logo height: 28–36px
- CTA button padding: `px-5 py-2.5` (20px horizontal, 10px vertical)

## Mobile Responsive Spacing

### Breakpoint Adjustments
| Property | Desktop (≥768px) | Mobile (<768px) |
|----------|------------------|------------------|
| Section padding top | 80–96px (`pt-20` to `pt-24`) | 48–56px (`pt-12` to `pt-14`) |
| Section padding bottom | 64–80px (`pb-16` to `pb-20`) | 40–48px (`pb-10` to `pb-12`) |
| Container side padding | 48–80px (`px-12` to `px-20`) | 20–24px (`px-5` to `px-6`) |
| Card padding | 32–48px (`p-8` to `p-12`) | 20–24px (`p-5` to `p-6`) |
| Grid gap | 24–32px (`gap-6` to `gap-8`) | 16–20px (`gap-4` to `gap-5`) |
| Button padding | `px-7 py-3.5` | `px-5 py-3` |

## Common Component Spacing Cheat Sheet

| Component | Property | Value | Tailwind |
|-----------|----------|-------|----------|
| Logo (nav) | height | 28–36px | `h-7` to `h-9` |
| Icon in card | margin-bottom | 16px | `mb-4` |
| Heading after icon | margin-top | 0 | — |
| Heading to body | margin-bottom | 8px | `mb-2` |
| Body to CTA | margin-top | 24–32px | `mt-6` to `mt-8` |
| Feature list items | gap | 12–16px | `gap-3` to `gap-4` |
| Section separator | border/margin | 0 / 80px | `my-20` |
| Avatar + name | gap | 12px | `gap-3` |
