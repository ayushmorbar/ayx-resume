# Contributing

## What to contribute
- Bug fixes (layout issues, compilation problems, package conflicts)
- Improvements to template DX (clearer config, better docs, safer placeholders)
- Additional optional sections/macros that don’t break the default one-page layout

## Guidelines
- Keep the default build **ATS-friendly** (conservative fonts, Unicode-extractable text).
- Keep **Template mode** safe by default:
  - Don’t put real personal data in `config/resume-config.template.tex` or `sections/*.tex`.
- Put examples/placeholders in `sections/*.tex` and real content in `sections/*.user.tex`.
- Avoid adding heavy dependencies unless they provide clear value.

## How to submit
1. Fork the repo
2. Create a feature branch
3. Make changes + ensure `main.tex` compiles
4. Open a pull request describing the change and why it helps
