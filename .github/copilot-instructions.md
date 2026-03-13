# Project Guidelines

## Code Style
- This project is a LaTeX template for Project and Bachelor theses at DHBW Mannheim.
- The root document is `LaTeX/master.tex`. All chapters and sections are referenced from here.
- Acronyms are managed in `LaTeX/acronyms.tex`. When referring to abbreviations in text, use the `\ac{}` or `\acp{}` commands.
- For bibliography, the framework uses the `biblatex` package combined with `biber` (do NOT use older `BibTeX` workflows). The main bibliography file is `LaTeX/bibliography.bib`.

## Architecture
- `LaTeX/`: Contains all raw `.tex` source files, configurations (`config.tex`), and images (`img/`).
- `LyX/`: Alternative template for users utilizing the LyX graphical editor.
- Configurable blocks, parameters, or sections to be completed by students are marked with `@stud` comments. 

## Build and Test
To compile the document (automatically resolving bibliography, glossaries, and references):
```bash
cd LaTeX
latexmk -pdf master.tex
```

## Conventions
- Do not make changes to `.tex` files that contradict the established DHBW Mannheim formatting without explicitly aligning with the user's requirements.
- Use `\autocite{}` for citations instead of simple `\cite{}` unless specific formatting is explicitly requested.
- When generating new chapters or sections, always prefer referencing them in `master.tex` using the `\input{}` command instead of merging everything into a monolithic file.
- For any new bibliography entries, ensure they are added to `bibliography.bib` with proper `biblatex` formatting and that the citation keys are consistent with the existing style (e.g., `AuthorYear` or `AuthorYearTitle`).
- When adding new acronyms, ensure they are defined in `acronyms.tex` and that the short form is unique and does not conflict with existing entries. They must be in alphabetical order.
- Allways use the Custom Agent **@Literature Researcher** for any research-related tasks. Use it everytime you write new content, to ensure that all statements are properly supported by scientific sources and that the bibliography is automatically updated. Never add Literature that was not found by the agent, and never add entries to the bibliography manually without using the agent.

## Writing Style
- The thesis should be written in German, following academic writing conventions.
- Use clear, concise language and avoid unnecessary jargon.
- Ensure that all sources are properly cited and that the bibliography is comprehensive and formatted correctly.
-  Use language that is typical of a Bachelors Student, without unnecessary complexity or overly formal academic tone.
- For Mathematical expressions, use the Notation described in the `vorraussetzungen.tex` chapter in the Notation section.

## Custom Agents
- **@Literature Researcher** (`.github/agents/researcher.agent.md`): Use this subagent whenever you need to find scientific literature, research new sources for the thesis, or automatically generate and insert new `biblatex` entries into `LaTeX/bibliography.bib`.

