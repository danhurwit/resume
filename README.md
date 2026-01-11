# Resume

Daniel Hurwit's resume in markdown format with PDF generation.

## Project Structure

```
resume/
├── README.md
├── hurwit_resume.pdf    # Generated PDF output
└── src/
    └── hurwit_resume.md # Source markdown file
```

## Dependencies

### Pandoc
Document converter for generating PDF from markdown.

**Install (Windows):**
```bash
winget install JohnMacFarlane.Pandoc --accept-source-agreements --accept-package-agreements
```

### MiKTeX
LaTeX distribution required by pandoc for PDF generation.

**Install (Windows):**
```bash
winget install MiKTeX.MiKTeX --accept-source-agreements --accept-package-agreements
```

> Note: After installing, you may need to restart your terminal or computer for PATH updates to take effect.

## Generate PDF

From the project root directory (PowerShell):

```powershell
pandoc src/hurwit_resume.md -o "hurwit_resume_$((Get-Date -Format 'MMM_yyyy').ToLower()).pdf" --template=src/resume-template.tex --pdf-engine=xelatex
```

Output: `hurwit_resume_jan_2026.pdf`
