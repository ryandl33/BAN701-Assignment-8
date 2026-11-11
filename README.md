# BAN 701 Assignment 8 - Dual-Approach Feature Implementation (AI-Assisted Track)

## Feature Specification: Excel Workbook Export
* **Feature Name:** Automated `.xlsx` Roster Export
* **Purpose:** Uses generative AI guidance (`openpyxl`) to export generated character rosters into a cleanly formatted Excel workbook saved directly to the user's Downloads directory.
* **Expected Behavior:** 
  1. Captures all characters generated during the active session.
  2. Writes headers and data rows into an active worksheet titled "Character Roster".
  3. Automatically calculates column widths to prevent clipped text.
  4. Generates a timestamped filename (`characters_YYYYMMDD_HHMMSS.xlsx`) and saves it securely to the local `Downloads` folder.
* **Tests Performed:**
  * *Test Case 1:* Generated a batch of characters, selected option 2, and verified a formatted `.xlsx` file was successfully created in the Downloads directory.
  * *Test Case 2:* Verified that auto-adjusted column widths properly fit all header and cell values without truncation errors.

---

## Feature Development Comparison: Manual vs. AI-Assisted Workflow

| Metric / Dimension | Manual Track (`manual-feature`) | AI-Assisted Track (`ai-feature`) |
| :--- | :--- | :--- |
| **Primary Tooling & Libraries** | Standard library (`os`, `glob`, `pathlib`, `random`) | Third-party library (`openpyxl`) via AI guidance |
| **Development Speed** | Slower; required manual syntax lookups for recursive directory traversal and relative path handling. | Faster; generative AI instantly provided working boilerplate for spreadsheet formatting and auto-width calculations. |
| **Code Structure & Ergonomics** | Focused on system-level path resolution and fallback error handling. | Focused on data presentation, workbook styling, and user file-system organization (`Downloads` path detection). |
| **Developer Experience** | High cognitive load on syntax correctness and debugging file paths manually. | Lower friction on boilerplate generation, allowing more focus on workflow integration and testing. |