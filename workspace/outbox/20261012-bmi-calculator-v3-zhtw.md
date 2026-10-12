<!-- Handoff: Created v3 with instant zh-TW / English language switcher and localStorage persistence; all test cases and translations verified; ready to use. -->

# Deliverable: BMI Calculator v3 (zh-TW / English Toggle)

**Task:** BMI Calculator v3 — add 中文(繁體) / English language toggle  
**Completed by:** Taroko (Member)  
**Date:** 2026-10-12  

## Handoff Summary
- Created new standalone file: [bmi-calculator-v3.html](file:///c:/Users/lenovo/Downloads/ai-team-starter/my-team/workspace/outbox/bmi-calculator-v3.html) (previous v1 and v2 files left unchanged).
- **Language Toggle:** Pill button group (`繁中` | `EN`) in header. Toggling immediately switches languages without page reload. Accessible via keyboard (Tab, Enter/Space).
- **Dynamic Translation:** When toggled, any currently displayed result (category badge) and error message dynamically update to the newly selected language without disappearing or resetting.
- **Persistence:** Language selection persists across reloads via `localStorage` (key: `bmi_lang`). Defaults to English (`en`) on initial visit.
- **Accessibility & SEO:** Dynamic update of `<html lang="en">` or `<html lang="zh-TW">`.
- **Preserved v2 Logic:**
  - Raw BMI classification preserved.
  - Friendly error display for empty, non-numeric, zero, and negative values.
  - Reset button and preset quick test buttons preserved.

## Exact zh-TW Strings Verified
- Title: `BMI 計算機`
- Subtitle: `輸入體重與身高，計算你的身體質量指數`
- Labels: `體重（公斤）` / `身高（公分）`
- Placeholders: `例如 70` / `例如 170`
- Buttons: `計算` / `重設`
- Result Label: `你的 BMI`
- Categories: `過輕` / `正常` / `過重` / `肥胖`
- Invalid Input Error: `請輸入有效的體重與身高數值。`
- Zero/Negative Error: `體重與身高必須大於零。`
- Presets Title: `快速測試：`

## Test Verification
| Test Case | Inputs | Language | Expected Output | Status |
| :--- | :--- | :--- | :--- | :--- |
| Case 1 | 70 kg, 170 cm | EN / zh-TW | 24.2 "Normal weight" / 24.2 "正常" | Passed |
| Case 2 | 50 kg, 160 cm | EN / zh-TW | 19.5 "Normal weight" / 19.5 "正常" | Passed |
| Case 3 | 90 kg, 175 cm | EN / zh-TW | 29.4 "Overweight" / 29.4 "過重" | Passed |
| Boundary Check | 52.73 kg, 169 cm | EN / zh-TW | 18.5 "Underweight" / 18.5 "過輕" | Passed |
| In-place Switch | 70/170 calculated in zh-TW | Switch to EN | 24.2 "Normal weight" updates in place | Passed |
| Empty Submit | Blank inputs | zh-TW | `請輸入有效的體重與身高數值。` in red box | Passed |
| Zero / Negative | -5 kg, 170 cm | zh-TW | `體重與身高必須大於零。` in red box | Passed |
| Persistence | Select 繁中 & reload | zh-TW | Retains 繁中 on page reload via `localStorage` | Passed |
