# README - BIP39 Printable Wordlist (A4).pdf

## Purpose
`BIP39 Printable Wordlist (A4).pdf` is a print-ready reference sheet for the standard BIP39 English word list.
It is designed for compact black-and-white printing and manual/offline workflows.

This PDF is generated from:
- `fou.ntain.com/pages/bip39_printer.html`

## Content Included
Each row in the PDF contains:
- Decimal word index (`0` to `2047`)
- BIP39 word (English list)
- Binary representation shown as 11 punched/not-punched dots

The 11 binary dot positions correspond to these values:
- `1024, 512, 256, 128, 64, 32, 16, 8, 4, 2, 1`

Legend:
- Black dot = punched (`1`)
- White dot = not punched (`0`)

## Layout Specification
- Paper size: `A4` portrait
- Visual style: minimal, black and white
- Columns per page: `4`
- Target words per page: `512`
- Rows are distributed across columns as evenly as possible.

### Spacing / readability choices
- Very compact text size for high density
- Dot groups are visually split as `4 + 4 + 3` to improve scanning
- Extra vertical spacing rhythm:
  - small gap every 5 lines
  - same-size gap every 10 lines

## Source of Truth
The BIP39 list is embedded in the HTML page and should match the official 2048-word English list.

If the list changes in code, regenerate the PDF and replace the published artifact.

## How to Generate the PDF
1. Open `fou.ntain.com/pages/bip39_printer.html` in a browser.
2. Click `Print / Save PDF`.
3. Use these print settings:
   - Paper: `A4`
   - Orientation: `Portrait`
   - Scale: `100%`
   - Margins: browser default or none (project-dependent)
   - Headers/footers: disabled
   - Background graphics: enabled if your browser requires it to keep filled dots fully black
4. Save as: `BIP39 Printable Wordlist (A4).pdf`.

## Validation Checklist
Before publishing, verify:
- Total words = `2048`
- First entry = `0 abandon`
- Last entry = `2047 zoo`
- Dot count per row = `11`
- Black dots print as solid black
- No unintended blank pages
- Column separators appear only where columns exist

## Recommended QA Pass
- Open PDF at 200% and confirm dot clarity and alignment.
- Print one physical page and verify:
  - dot fill visibility
  - line spacing readability
  - no clipping at right edge
  - consistent row rhythm

## Versioning Guidance
When updating layout or typography:
1. Regenerate the PDF
2. Bump release note/changelog entry
3. Keep filename stable unless format meaningfully changes

Suggested naming if versioning is needed:
- `BIP39 Printable Wordlist (A4) vYYYYMMDD.pdf`

## Security/Operational Notes
- This PDF is a reference print artifact only.
- Do not store private seed phrases inside this file.
- Do not annotate operational secrets in shared copies.

## License
See `LICENSE` (MIT License).

