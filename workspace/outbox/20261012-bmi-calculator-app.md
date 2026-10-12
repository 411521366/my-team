<!-- Handoff: Built the BMI calculator app in single-file HTML at workspace/outbox/bmi-calculator.html; all 3 test cases and bad-input handling verified; ready to use. -->

# Deliverable: BMI Calculator App

**Task:** Build a BMI Calculator App  
**Completed by:** Taroko (Member)  
**Date:** 2026-10-12  

## Handoff Summary
- Built self-contained HTML/CSS/JS file: [bmi-calculator.html](file:///c:/Users/lenovo/Downloads/ai-team-starter/my-team/workspace/outbox/bmi-calculator.html)
- Implemented formula `BMI = weight (kg) / (height (m))²` with cm-to-m conversion and rounding to 1 decimal place.
- Implemented category classifications:
  - Below 18.5 → "Underweight"
  - 18.5 – 24.9 → "Normal weight"
  - 25.0 – 29.9 → "Overweight"
  - 30.0 and above → "Obese"
- Input validation: friendly error message displayed for empty, non-numeric, zero, or negative numbers without crashing.
- Ready to use: Can be opened directly in any browser.

## Test Verification
| Test Case | Inputs | Expected Output | Status |
| :--- | :--- | :--- | :--- |
| Case 1 | 70 kg, 170 cm | BMI ≈ 24.2, Normal weight | Passed |
| Case 2 | 50 kg, 160 cm | BMI ≈ 19.5, Normal weight | Passed |
| Case 3 | 90 kg, 175 cm | BMI ≈ 29.4, Overweight | Passed |
| Bad Input | Non-numeric / Negative | Friendly error message | Passed |
