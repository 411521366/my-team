<!-- Handoff: Created v2 deliverable addressing both send-back fixes (raw BMI category lookup and empty-input error box display); verified edge cases; ready to use. -->

# Deliverable: BMI Calculator v2 (Fixes Applied)

**Task:** BMI Calculator — 2 fixes for v2  
**Completed by:** Taroko (Member)  
**Date:** 2026-10-12  

## Handoff Summary
- Created new version file without overwriting v1: [bmi-calculator-v2.html](file:///c:/Users/lenovo/Downloads/ai-team-starter/my-team/workspace/outbox/bmi-calculator-v2.html)
- **Fix 1 Applied:** Classified BMI category using the raw calculated `bmi` float, while displaying the formatted 1-decimal-place value. A raw BMI of 18.46 (e.g. 52.73 kg / 169 cm) correctly classifies as "Underweight" with the displayed rounded value of 18.5.
- **Fix 2 Applied:** Removed native `required` attribute from inputs and added `novalidate` to prevent browser popups. Submitting empty inputs now reliably displays the friendly error message: *"Please enter valid numerical values for both weight and height."*
- Original version preserved intact at [bmi-calculator.html](file:///c:/Users/lenovo/Downloads/ai-team-starter/my-team/workspace/outbox/bmi-calculator.html).

## Test Verification
| Test Case | Inputs | Expected Output | Status |
| :--- | :--- | :--- | :--- |
| Case 1 | 70 kg, 170 cm | BMI ≈ 24.2, Normal weight | Passed |
| Case 2 | 50 kg, 160 cm | BMI ≈ 19.5, Normal weight | Passed |
| Case 3 | 90 kg, 175 cm | BMI ≈ 29.4, Overweight | Passed |
| Boundary Check | 52.73 kg, 169 cm (raw ~18.46) | BMI 18.5, Underweight | Passed |
| Empty Submit | (Both blank) | Friendly error message in red box | Passed |
| Invalid Input | Non-numeric or negative | Friendly error message in red box | Passed |
