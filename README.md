# Avery 8160

Print address labels on Avery 8160 sheets from data pasted out of a Google Sheets spreadsheet.

A single HTML page with no build step, no dependencies, and no server. Your data never leaves the browser.

## Usage

1. Open `index.html` in a web browser.
2. In Google Sheets, select the cells you want (including the header row, if there is one) and copy them (⌘C / Ctrl+C).
3. Paste into the text area on the page.
4. Uncheck any columns that should not appear on the labels (e.g. email or phone). Uncheck "First row is a header row" if your selection has no header.
5. Check the label preview, then print.

Each label is built from the checked columns, in spreadsheet order, one value per line. Empty cells are skipped.

## Printing

For the addresses to line up with the labels:

- Set **Scale** to **100%** (not "Fit to page").
- Turn off **Headers and footers**.
- Use **Letter** paper.

Only the label sheets are printed; the rest of the page is hidden. Before using a label sheet, print a test page on plain paper and hold it against a label sheet to check alignment.

## Label layout

Avery 8160 (also 5160 and compatible) on US Letter, 8.5″ × 11″:

| Measurement       | Value                    |
| ----------------- | ------------------------ |
| Labels per page   | 30 (3 columns × 10 rows) |
| Label size        | 2⅝″ × 1″                 |
| Top/bottom margin | ½″                       |
| Side margin       | 3⁄16″                    |
| Column gap        | ⅛″                       |
| Row gap           | none                     |

These values are defined in inches in the `.sheet` and `.label` CSS rules in `index.html`.
