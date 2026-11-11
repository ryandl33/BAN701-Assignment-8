# Sci-Fi Character Generator
BAN701 – Assignment 8

## Project Description
A simple Python program that generates random sci-fi characters for tabletop games. Each character gets a name, pronouns, background details, stats, and a randomly assigned portrait image reference.

## Initial Version
- **Random name and pronouns:** Picks a name from a list and assigns pronouns based on a dice roll.
- **Background details:** Randomly selects an occupation, home planet or station, motivation, and quirk.
- **Stats:** Rolls STR, SPD, INT, and COMBAT (2d10 + 25).
- **Saves:** Rolls Sanity, Fear, and Body (2d10 + 10).
- **Health:** Rolls HP (1d10 + 10).
- **Menu:** Lets the user generate a character, export characters, or exit.

## AI Tool Used
Claude (Anthropic)

## AI Assistance
Used for CSV export and quantity input logic, plus debugging guidance.

## New or Modified Features (Manual-Feature Branch)
- **Random Portrait Image Assignment:** Recursively scans local subfolders (`images/100 Android Faces` and `images/100 Human sci-fi faces`) to randomly assign a character portrait file path to each generated record.

### Feature Specification: Random Portrait Assignment
- **Feature Name:** Automated Random Image Assignment
- **Purpose:** Automatically scans local asset directories and attaches a unique, random portrait path to every character record.
- **Expected Behavior:** Locates the `images/` directory using absolute script paths, discovers valid image files recursively across subfolders, and selects one at random.
- **Test Cases:**
  1. *Test Case 1:* Generate 1 character; verify an absolute file path pointing to a valid image in the subfolders is included in the output.
  2. *Test Case 2:* Generate 25 characters; verify unique random images are assigned across the batch without errors.

## Evaluation of AI Output
Accepted CSV export and quantity input after testing. Kept timestamped filenames to prevent overwriting.

## How to Run the Program
1. Install Python 3 and dependencies (`pip install openpyxl pillow`).
2. Download or clone this repository and ensure an `images/` folder with subfolders is present.
3. Run: `python main.py`