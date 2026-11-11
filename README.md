# BAN 701 Assignment 9 - Dual-Approach Feature Implementation

## Project Overview
This repository demonstrates a dual-approach development workflow, comparing a manual coding approach against an AI-assisted approach across two isolated feature branches (`manual-feature` and `ai-feature`).

---

## Feature Development Comparison

### Feature Overview & Approaches
* **Manual Branch (`manual-feature`):** Implemented an automated random portrait image assignment feature using only Python’s standard libraries (`os`, `glob`, `pathlib`, `random`). This required writing custom path-traversal logic to recursively discover asset subfolders.
* **AI Branch (`ai-feature`):** Implemented an Excel (`.xlsx`) roster export feature using the third-party `openpyxl` library guided by generative AI.

### AI Code Evaluation & Modifications
* **First-Attempt Accuracy:** The AI-produced `openpyxl` export code was functional overall but required a minor adjustment on the first attempt regarding operating system path resolution for the local `Downloads` directory.
* **Modified / Rejected Code:** The initial snippet generated a hardcoded file path; it was modified to dynamically detect the OS environment (Windows vs. Unix) and implement auto-adjusted column width logic to ensure proper data formatting and prevent visual truncation.

### Confidence & Reflection
The manual approach provided greater confidence in foundational system-level handling (such as raw file paths and error management), while the AI approach significantly accelerated third-party library integration and boilerplate data styling. Combining both workflows highlighted how AI excels at rapid library implementation, whereas manual coding deepens structural control.