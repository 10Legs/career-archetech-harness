---
description: Generate a visually appealing PDF resume from a Markdown file
argument-hint: [input-md-path] [output-pdf-path]
allowed-tools: [Read, Write, Edit, Glob, Shell]
---

# Generate PDF Resume

This command converts your Markdown resume into a professionally styled PDF using a custom executive theme.

## Prerequisites

To generate high-quality PDFs with CSS support, we recommend using `md-to-pdf`. 

If you don't have it installed, run:
`npm install -g md-to-pdf`

## Execution

1. **Input Selection**: 
   - If `input-md-path` is not provided, look for `resume.md` in the most recent job target directory.
2. **Style Selection**:
   - Default style: `patterns_library/pdf-styles/resume.css`
3. **Conversion**:
   - Run the conversion tool:
     `md-to-pdf [input-md-path] --stylesheet patterns_library/pdf-styles/resume.css --pdf-options '{ "format": "A4", "margin": "1in" }'`
4. **Output**:
   - Save the resulting PDF to `[output-pdf-path]`.

## Success Criteria

- [ ] PDF generated successfully
- [ ] CSS styles applied correctly (Verified by checking for tool success output)
- [ ] PDF saved to the correct location

## Troubleshooting

- **Fonts**: If the PDF looks "plain," ensure the fonts in `resume.css` are available on your system.
- **Tooling**: If `md-to-pdf` fails, ensure you have a modern version of Node.js installed.
