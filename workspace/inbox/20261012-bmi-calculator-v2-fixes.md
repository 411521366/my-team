# Send-back: BMI Calculator — 2 fixes for v2

**From:** Wailan (Leader) → Taroko (Member)
**Date:** 2026-10-12
**Regarding:** `workspace/outbox/bmi-calculator.html` (your first version passed all test cases — this is polish, not a redo)

## What to do
Make a **new file** `bmi-calculator-v2.html` in `workspace/outbox/` (do NOT overwrite v1). Same app, plus these two fixes:

### Fix 1 — Classify on the raw BMI, not the rounded one
- **Problem:** The category is chosen from `roundedBmi`. Example: a real BMI of 18.46 rounds to 18.5 and gets labeled "Normal weight" even though it is actually Underweight.
- **Change:** Decide the category using the raw `bmi` value, then display the rounded value. The displayed number and label must always agree with the standard cutoffs (18.5 / 25 / 30).

### Fix 2 — Let the custom error message show for empty input
- **Problem:** The inputs have the `required` attribute, so the browser blocks an empty submit before `calculateBMI()` runs, and the friendly error message never appears.
- **Change:** Remove `required` from both inputs (keep the JS validation, which already handles empty / non-numeric / zero / negative). Empty submit should now show: "Please enter valid numerical values for both weight and height."

## Format
Same single-file HTML approach, file name `bmi-calculator-v2.html`, saved in `workspace/outbox/`.

## What "done" looks like
- The three original test cases still pass: 70/170 → 24.2 Normal, 50/160 → 19.5 Normal, 90/175 → 29.4 Overweight.
- New check: BMI of 18.46 (e.g. 53 kg / 169 cm) shows BMI 18.5 **with label "Underweight"** — number rounded, label from raw value.
- Submitting with both fields empty shows the friendly error message in the red box, not a browser popup.
- Bad input (letters, zero, negative) still handled without crashing.
