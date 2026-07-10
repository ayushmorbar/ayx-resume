# ayx-resume (LaTeX Resume Template, ATS-friendly)

**Author:** Ayush Morbar (`https://github.com/ayushmorbar`)

**Repository:** `https://github.com/ayushmorbar/ayx-resume`

This is a public, MIT-licensed resume template. You’re free to use, modify, and redistribute it (see `LICENSE`). Suggestions and contributions are welcome via GitHub issues and pull requests.

This repo supports two modes (so you can keep the public template pristine while editing your real resume in the same project):
- **Template mode**: renders example content + placeholder identity
- **User mode**: renders your real content + real identity

## Quick start
1. Open `config/resume-config.tex` and set one of:
   - `\TemplateModetrue`  (template/examples)
   - `\TemplateModefalse` (your resume)
2. Edit your details in `config/resume-config.user.tex` (name, phone, email, links, metadata, toggles).
3. Edit your content in `sections/*.user.tex`.
4. Compile with **pdfLaTeX** (recommended).

## Use on Overleaf
1. Download this repo as a ZIP (or clone it).
2. In Overleaf: New Project > Upload Project > Upload `.zip`.
3. Set `main.tex` as the root document if Overleaf doesn’t pick it automatically.
4. Compile with **pdfLaTeX**.

If you publish this as an Overleaf template, please keep the attribution to Ayush Morbar and the MIT license intact.

## Template design goals
- **Safe by default**: no real personal data required to build.
- **Good DX**: clean macros, reusable section structure.
- **ATS-friendly**: Unicode-extractable text; conservative font choices.

## File map
### Entry point
- `main.tex` — main resume document.

### Config
- `config/resume-config.tex` — wrapper that selects template vs user config (usually only the mode switch changes).
- `config/resume-config.template.tex` — template placeholders (don’t edit).
- `config/resume-config.user.tex` — your real identity/contact/toggles (edit freely).

### Template internals
- `core/resume-style.tex` — packages + layout/styling.
- `core/resume-macros.tex` — template commands.

### Sections
- Template/example sections: `sections/*.tex`
- Your real sections: `sections/*.user.tex`

## Section toggles
Optional sections are controlled in `config/resume-config.user.tex` (and template defaults live in the template config):
- `\IncludeCertificationstrue/false`
- `\IncludeAwardstrue/false`
- `\IncludeLeadershiptrue/false`
- `\IncludePublicationstrue/false`

## ATS vs “pretty” links
In your config file:
- `\ATStrue`  → text-only header + text project links (more ATS-friendly)
- `\ATSfalse` → icon header + icon project links

## Optional project links
Use `\ProjectLinksAuto{<github-url>}{<demo-url>}` to auto-select text vs icons based on the ATS toggle.

## Publishing checklist (recommended)
- Keep `\TemplateModetrue` (and template placeholders) as the default on the public branch.
- Put real data only in `config/resume-config.user.tex` + `sections/*.user.tex`.
- If publishing publicly, consider keeping your real resume on a private branch/repo.

## Attribution
This template is maintained by Ayush Morbar.

Originally forked/inspired by Jake Gutierrez’s resume template (see `archive/jake.tex`).
not to
## License
MIT (see `LICENSE`).
