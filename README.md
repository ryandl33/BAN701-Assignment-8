# Sci-Fi Character Generator
BAN701 – Assignment 8

## Project Description
A simple Python program that generates random sci-fi characters for tabletop games. Each character gets a name, pronouns, background details, and stats.

## Initial Version
- **Random name and pronouns:** Picks a name from a list and assigns pronouns based on a dice roll.
- **Background details:** Randomly selects an occupation, home planet or station, motivation, and quirk.
- **Stats:** Rolls STR, SPD, INT, and COMBAT (2d10 + 25).
- **Saves:** Rolls Sanity, Fear, and Body (2d10 + 10).
- **Health:** Rolls HP (1d10 + 10).
- **Menu:** Lets the user generate a character, view the export option (not available yet), or exit. Invalid input shows an error message.

## AI Tool Used
Claude (Anthropic)

## AI Assistance
I used Claude to help add two features: exporting characters to a CSV file and generating multiple characters at once. I also used it for debugging guidance.

## New or Modified Features
- **Export to CSV (option 2):** Saves every character generated during the session to a timestamped CSV file that opens in Excel.
- **Custom quantity (option 1):** Asks how many characters to generate (1–100) and validates the input, re-asking if it's not a whole number in range.

## Evaluation of AI Output
I accepted the CSV export and quantity input after testing them. I kept the timestamped filenames so each export creates a new file instead of overwriting the previous one. I kept the 100-character limit because generating more than that at once would be impractical.

While integrating the export, I left an "Exported to CSV" message in the menu, then removed it because the export function already prints its own result, and the extra message showed even when nothing was exported.

## How to Run the Program
1. Install Python 3.
2. Download or clone this repository.
3. Open a terminal in the project folder.
4. Run: `python main.py`
5. Enter a menu number to choose an option.