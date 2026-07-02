# DiagCAPL Suite

## Structure
```
diagcapl_suite/
├── index.html          ← Landing page (open this first)
├── generator.html      ← DiagCAPL CAPL Generator (v74)
├── report.html         ← CANoe.DiVa Report Tool (needs setup - see below)
├── bg.jpg              ← Background image (place the car diagnostic image here)
├── apply_report.py     ← Patches the report tool automatically
└── README.md
```

## Setup Steps

### 1. Place background image
Copy your diagnostic/automotive background image as `bg.jpg` in this folder.
The landing page and report tool will use it as a subtle overlay.

### 2. Set up the Report Tool
The report tool (document 5 from the conversation) needs to be saved as `report.html`.
Run the patch script to apply DiagCAPL colour scheme:

```bash
python3 apply_report.py <path_to_canoe_diva_report.html>
```

This will:
- Remove the "CANalyzer Write Window Analyser" eyebrow tag
- Update colours: cyan #00d4ff, amber #f59e0b, green #10b981, red #ef4444
- Add DiagCAPL home link in topbar
- Change copyright year to 2026
- Add background image overlay

### 3. Open index.html in browser
All navigation links between the three tools work via relative paths.

## Colour Palette
| Token | Hex | Usage |
|-------|-----|-------|
| Accent | #00d4ff | Primary cyan, highlights |
| Amber | #f59e0b | Warnings, gold accents |
| Green | #10b981 | Pass states |
| Red | #ef4444 | Fail states |
| Ink | #07080b | Page background |

## Fonts
- **Syne 800** — Display headings
- **Space Grotesk** — Body text
- **JetBrains Mono / Share Tech Mono** — Code, labels
