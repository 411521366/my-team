# Task: BMI Calculator v3 — add 中文(繁體) / English language toggle

**From:** Wailan (Leader) → Taroko (Member)
**Date:** 2026-10-12
**Base:** `workspace/outbox/bmi-calculator-v2.html` (both fixes already verified — keep them working)
**Language:** This note is in English; the zh-TW strings are specified below.

## What to do
Add a language toggle so the whole UI can be shown in **English** or **繁體中文 (Traditional Chinese, Taiwan)**. Keep the current clean design — this is NOT a Duolingo-style redesign.

## Requirements
1. **New file:** `workspace/outbox/bmi-calculator-v3.html` (never overwrite v1 or v2).
2. Add a language switcher in the header, e.g. a small pill button group: `繁中` | `EN`.
   - Toggling must instantly translate the UI without reloading the page.
   - The already-calculated result (if shown) must also switch language, not disappear.
3. All user-visible text must be translated. Use exactly these zh-TW strings (Taiwan usage):
   - Title: `BMI 計算機`
   - Subtitle: `輸入體重與身高，計算你的身體質量指數`
   - `體重（公斤）` / `身高（公分）`
   - Placeholders: `例如 70` / `例如 170`
   - Buttons: `計算` / `重設`
   - Result label: `你的 BMI`
   - Categories: `過輕` / `正常` / `過重` / `肥胖`
   - Error (invalid input): `請輸入有效的體重與身高數值。`
   - Error (zero/negative): `體重與身高必須大於零。`
   - Test section title: `快速測試：`
4. Persist the choice in `localStorage` so the chosen language survives a page reload. Default = English on first visit.
5. Set `<html lang>` to `zh-TW` or `en` to match the selected language (good for accessibility and search engines).
6. Keep ALL existing behavior from v2: raw-BMI classification, friendly empty-submit error (no `required` attr), validation, reset, preset chips. Preset chip labels may stay in Latin ("70kg / 170cm") in both languages.
7. Keyboard: the toggle must be reachable and operable via Tab + Enter/Space.

## Format
Single self-contained HTML file, no external libraries, zh-TW strings written as UTF-8 (file must be saved UTF-8 or Chinese will show as garbage).

## What "done" looks like
- Open v3 → English UI by default.
- Click `繁中` → all labels above turn into the zh-TW strings listed; click `EN` → back to English. No page reload either way.
- Calculate 70/170 while in 繁中 → BMI 24.2 + `正常`; then switch to EN → same number, "Normal weight".
- Reload the page → language stays as last chosen.
- v2 test cases still pass in BOTH languages: 50/160 → 19.5 正常/Normal, 90/175 → 29.4 過重/Overweight, boundary 52.73/169 → 18.5 過輕/Underweight, empty submit → zh-TW error in 繁中 mode, letters/negative → error, no crash.
