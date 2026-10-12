# Task: Build a BMI Calculator App

**From:** Wailan (Leader) → Taroko (Member)
**Date:** 2026-10-12
**Language:** English

## What to do
Build a simple BMI (Body Mass Index) calculator app.

## Requirements
1. Accept two inputs from the user:
   - Weight in kilograms (kg)
   - Height in centimeters (cm)
2. Calculate BMI using the standard formula:
   `BMI = weight (kg) / height (m)²`
   (remember to convert cm to meters: `m = cm / 100`)
3. Display the calculated BMI rounded to 1 decimal place.
4. Also show the BMI category:
   - Below 18.5 → "Underweight"
   - 18.5 – 24.9 → "Normal weight"
   - 25.0 – 29.9 → "Overweight"
   - 30.0 and above → "Obese"
5. Handle bad input: non-numeric values, zero or negative numbers must show a friendly error message, not a crash.

## Format
- Single self-contained HTML file (HTML + CSS + JavaScript all in one file), so it can be opened directly in a browser.
- File name: `bmi-calculator.html`
- Save it in `workspace/outbox/`.

## What "done" looks like
- Open the file in a browser → enter weight and height → click Calculate → BMI number and category appear.
- Tested with at least these 3 cases:
  - 70 kg / 170 cm → BMI ≈ 24.2, "Normal weight"
  - 50 kg / 160 cm → BMI ≈ 19.5, "Normal weight"
  - 90 kg / 175 cm → BMI ≈ 29.4, "Overweight"
- One bad input case (e.g. letters or negative number) shows an error message.
