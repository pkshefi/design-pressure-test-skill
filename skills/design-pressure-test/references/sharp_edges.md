# Design Pressure Test — Sharp Edges

Common whitespace and spacing failures that hurt design quality. Each entry includes severity, symptom, why it fails, and the fix.

---

## Uneven Card Padding

### **Severity**: critical
### **Symptom**: Card content touches edges on one axis but has excess space on the other
### **Why it fails**: Uneven padding signals lack of polish and makes the card feel inconsistent. Users subconsciously register the imbalance as low quality.
### **Fix**: Ensure padding is equal on all sides (`p-6` or `p-8`, not `px-4 py-8`). If directional padding is needed, use semantic tokens (e.g., `px-6 py-8` for cards with prominent bottom CTAs).

---

## Zero Grid Gap

### **Severity**: critical
### **Symptom**: Grid items visually merge — no gap between cards, features, or columns
### **Why it fails**: Items bleed into each other, destroying visual hierarchy. The user can't tell where one item ends and another begins.
### **Fix**: Always set `gap-6` (24px) or `gap-8` (32px) on grids. Never rely on margins alone.

---

## Icon Touching Text

### **Severity**: high
### **Symptom**: Icon is flush against adjacent text with less than 8px clearance
### **Why it fails**: The icon and text visually merge, reducing readability and making the layout feel cramped.
### **Fix**: Set minimum `gap-2` (8px) between icons and text. For feature lists with icons, use `flex gap-3` (12px).

---

## Button Labels Too Tight

### **Severity**: high
### **Symptom**: Button text nearly touches the left/right edge of the button with less than 12px padding
### **Why it fails**: Tight button padding looks cheap and makes the button harder to tap on mobile. It's the most common spacing mistake.
### **Fix**: Minimum `px-4` (16px) for small buttons, `px-7` (28px) for large buttons. For primary CTAs, use `px-8` (32px).

---

## Section Bleeding

### **Severity**: high
### **Symptom**: Two adjacent sections with no visual separation — 24px or less between them
### **Why it fails**: The visitor can't tell when one section ends and another begins. Page feels like one continuous block of content.
### **Fix**: Minimum `py-16` (64px) between sections. Use `py-20` (80px) as standard. For major transitions, use `py-24` (96px).

---

## Missing Spatial Rhythm

### **Severity**: high
### **Symptom**: Section padding, card padding, and margins use arbitrary values (e.g., 23px, 37px, 52px)
### **Why it fails**: Inconsistent values violate the 8pt grid system. The eye detects subtle misalignment even if the conscious mind doesn't.
### **Fix**: Stick to 8pt increments: 8, 16, 24, 32, 40, 48, 64, 80, 96px. Use Tailwind/shadcn tokens which follow this system.

---

## Hero Section with No Top Padding

### **Severity**: high
### **Symptom**: Hero content starts at the very top of the page with little or no padding from the browser edge
### **Why it fails**: The hero is the most important section — it needs room to breathe. Content flush to the top feels rushed and low-value.
### **Fix**: Minimum `pt-20` (80px) for the hero. For landing pages, use `pt-24` (96px).

---

## Form Fields Too Dense

### **Severity**: medium
### **Symptom**: Less than 16px gap between form fields; labels too close to inputs
### **Why it fails**: Dense forms increase cognitive load and feel like work. Users abandon forms that look tedious.
### **Fix**: Use `space-y-5` (20px) or `space-y-6` (24px) between fields. Keep 4px (`mb-1`) between label and input.

---

## Container Full Width (No Constraint)

### **Severity**: medium
### **Symptom**: Content stretches 100% width on large screens, creating unwieldy 120+ character line lengths
### **Why it fails**: Excessively wide text is hard to read. The design loses structure without a container constraint.
### **Fix**: Set `max-w-7xl` (1280px) or `max-w-6xl` (1152px) as the content container. For text-heavy sections, use `max-w-prose` (650px).

---

## Mobile Padding Collapse

### **Severity**: medium
### **Symptom**: Container padding on mobile is less than 16px; content touches screen edges
### **Why it fails**: On mobile, every pixel counts. Less than 16px side padding makes text hard to read and the layout look broken.
### **Fix**: Minimum `px-5` (20px) on mobile. Use responsive padding: `px-6 md:px-12 lg:px-20`.

---

## CTA Clustering

### **Severity**: medium
### **Symptom**: Multiple CTAs (primary + secondary + text link) stacked within 16px of each other
### **Why it fails**: Too many actions too close together causes decision paralysis. Each CTA devalues the others.
### **Fix**: At least `gap-4` (16px) between CTAs. If more than two CTAs, split them across the page or use progressive disclosure.

---

## Image Margin Missing

### **Severity**: medium
### **Symptom**: An image or illustration touches adjacent text or the edge of its container
### **Why it fails**: Images without margin look like they were placed by accident. The layout lacks intentionality.
### **Fix**: `mb-6` (24px) or `mb-8` (32px) below images. For inline images, `mx-auto` with `my-8`.

---

## Excessive Whitespace

### **Severity**: low
### **Symptom**: Content appears sparse; too much empty space between elements (e.g., 160px between every section)
### **Why it fails**: Yes, too much whitespace is also a problem. The user has to scroll excessively, and the page feels empty.
### **Fix**: Use `py-12` (48px) to `py-16` (64px) for standard sections. Reserve `py-20`+ for hero and final CTA only.

---

## Price + CTA Too Close

### **Severity**: medium
### **Symptom**: The pricing amount and the CTA button have less than 20px gap
### **Why it fails**: The visitor sees the price and immediately sees the action — no room to process value. This increases price anxiety.
### **Fix**: `mt-8` (32px) between price and CTA button. Add a feature checklist in between to reinforce value.

---

## No Gap Between Logo and Nav CTA

### **Severity**: low
### **Symptom**: Logo and CTA button in the nav are separated by elements in between, but not pushed to opposite ends
### **Why it fails**: The nav doesn't use `justify-between` from flexbox — the logo is near the CTA, leaving dead space.
### **Fix**: Use `flex justify-between items-center` on the nav wrapper. Logo left, CTA right.
