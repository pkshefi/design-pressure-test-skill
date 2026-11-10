# Design Pressure Test — Validations

Machine-readable rules for automated spacing checks.

## Section Padding Missing

### **Id**: section-padding-missing
### **Severity**: error
### **Type**: regex
### **Pattern**: `section\s*{` (without padding)
### **Suggestion**: Every section must have explicit vertical padding (`py-16` minimum).

## Container Missing Max-Width

### **Id**: container-maxwidth-missing
### **Severity**: warning
### **Type**: regex
### **Pattern**: `.container\s*{` or `max-w-` (looking for missing)
### **Suggestion**: Content containers should constrain width (`max-w-6xl` or `max-w-7xl`).

## Uneven Card Padding

### **Id**: uneven-card-padding
### **Severity**: error
### **Type**: regex
### **Pattern**: `px-[0-9]+.*py-[0-9]+` where px and py differ by more than 2 tokens
### **Suggestion**: Card padding should be equal on all sides unless there's a clear semantic reason.

## Icon-Text Gap Too Small

### **Id**: icon-text-gap
### **Severity**: warning
### **Type**: regex
### **Pattern**: `gap-[0-2]` in flex containers with icon + text
### **Suggestion**: Minimum `gap-2` (8px) between icons and text.

## Button Padding Insufficient

### **Id**: button-padding-small
### **Severity**: warning
### **Type**: regex
### **Pattern**: `px-[0-3]` on button elements
### **Suggestion**: Minimum `px-4` (16px) for small buttons, `px-7` (28px) for large buttons.

## Mobile Padding Collapse

### **Id**: mobile-padding-missing
### **Severity**: error
### **Type**: regex
### **Pattern**: Container or section with no `px-` value under 768px breakpoint
### **Suggestion**: Side padding must be at least 16px on mobile (`px-4` minimum, `px-5` recommended).

## Section Gap Too Small

### **Id**: section-gap-small
### **Severity**: warning
### **Type**: regex
### **Pattern**: Consecutive sections with less than `py-8` between them
### **Suggestion**: Minimum 32px (`py-8`) between sections. Standard is 64px (`py-16`).

## Zero Grid Gap

### **Id**: grid-gap-zero
### **Severity**: error
### **Type**: regex
### **Pattern**: `grid` class without `gap-` class in the same element
### **Suggestion**: Grid layouts must have explicit gap (`gap-6` or `gap-8`).

## No Vertical Rhythm

### **Id**: vertical-rhythm-missing
### **Severity**: warning
### **Type**: pattern
### **Pattern**: Heading followed by body text without consistent margin
### **Suggestion**: Use consistent `mb-2` for heading-to-body spacing, `mb-4` for heading-to-subheading.

## CTA Cluster Detection

### **Id**: cta-cluster
### **Severity**: warning
### **Type**: pattern
### **Pattern**: More than 2 CTAs within 32px vertical space
### **Suggestion**: If multiple CTAs are needed, at least 16px gap between them. Consider using only one primary CTA.
