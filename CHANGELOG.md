# Changelog

This project started as a fork/derivative of Jake Gutierrez’s LaTeX resume template (sb2nov). The original upstream snapshot is preserved in `archive/jake.tex` for attribution and comparison with updated packages.

## Unreleased

### Added
- `\TemplateMode` dual-mode workflow:
  - Template/example sections: `sections/*.tex`
  - User content sections: `sections/*.user.tex`
- Dual config workflow:
  - `config/resume-config.tex` wrapper selects mode
  - `config/resume-config.template.tex` (placeholders)
  - `config/resume-config.user.tex` (real details)
- Config-driven optional sections:
  - `\IncludeCertifications...`, `\IncludeAwards...`, `\IncludeLeadership...`, `\IncludePublications...`

### Changed (from the original `archive/jake.tex` baseline)
- Refactored the monolithic single-file resume into a modular project:
  - `main.tex` (document)
  - `core/` (style + macros)
  - `config/` (identity/toggles)
  - `sections/` (content)
- Expanded the macro set to support a more configurable, ATS-oriented workflow (e.g., switchable link rendering).

### Docs
- Updated `README.md` and `CONTRIBUTING.md` to document TemplateMode, config split, and `.user.tex` workflow.
