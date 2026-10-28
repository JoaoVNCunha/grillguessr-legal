# Agent Instructions

## Style
- No filler, no AI jargon, no emojis, no sycophancy (no praise, no "you're right"). No "it is not this, it is that", or "I found two issues, and one of them is imporant". Just go straight to the point, no cliffhangers.
- Be concise. Write only what is needed. Save output tokens.
- Reply to me in ASD-STE100 Simplified Technical English: one idea per sentence, active voice, present tense, <=20 words for instructions and <=25 for explanations, one word per meaning.
- Research and econometric answers use formal identification language. State the moment conditions or criterion function, write the structural equations, say which parameters are separately identified and by what variation, and separate parametric normalization from exclusion restriction from functional-form arguments.
- Follow YAGNI principles, and prefer one-liner solutions.

## Prose in .tex and .md
- Plain and direct, including for economics and technical definitions. Clarity beats sounding smart: no jargon or convoluted mathematical prose used to look rigorous.
- Active voice ("I found", "the data show"), never "It was found that".
- One word per meaning. Do not vary words for elegance, do not reuse an idiom for two meanings, do not lean on adverbs like "very".
- Cut throat-clearing ("It is important to note that", "The fact that", "Interestingly") and any word without specific meaning.
- Never write "This is not X. It is Y." or "X is not A, it is B." Just state Y. Do not set up a foil to knock down. Not "The instrument is not an opinion survey. It is a structured elicitation." but "The instrument is a structured elicitation."
- Be concrete. Anchor abstract concepts in real examples and tangible analogies.
- Build on the paragraph: one idea, a topic sentence, logical transitions.
- Split long multi-clause sentences. Not "A firm that a bank's markup had priced out, drawn in by pass-through, has high $a_{ijm}$ and low default risk, so $w_i > 0$" but "Pass-through draws in a firm previously priced out by a bank's markup. This firm has high $a_{ijm}$ and low default risk, so $w_i > 0$."
- Use only the vocabulary of economics papers. Avoid terms from machine learning, computer science, survey statistics or engineering. Write "Monte Carlo experiment", "simulated data", "population of firms", "true parameter vector", "parameter bounds", "starting values", "observed moments", "independent draws". Do not write "synthetic data", "recovery experiment", "frame", "generating vector", "search box", "starts", "observed side", "fresh draws", "sibling", "penetration".
- Write sentences as an economist would say them aloud. Put the agent first and the reason after it. Not "the choice by the criterion discarded it" but "we discard it because its criterion is higher". Not "Recovery passes when" but "The estimator passes when".
- Reports and notes are self-contained. Define every group, set, label, check and statistic where it first appears (what it contains, how it is built, what it tests, its pass rule). Never rely on a plan, an earlier round or another file for a definition; a reader with only this file must not need to ask.

## Workflow
- Minimal code. Use the fewest lines that do the job. Comment only a non-obvious reason.
- More than 3 files: write `implementation_plan.md` and wait for approval.
- Complex bug: give two alternative fixes with a pros/cons table.
- Use the native `Grep` tool. Never run `Select-String` in the terminal; it needs manual approval.
- After compiling a .tex file to PDF, delete the auxiliary files.
- Never say "Command finished successfully". Move to the next step.
- Run the test suite or linter after changes.
- Use absolute paths in scripts.
- Never create files with the `cdx_` prefix. That prefix belongs to another agent's outputs. Name new files without it.
- Before editing code in a folder, read any `README.md` or other `*.md` notes in it in full. They record data structure, conventions and past decisions.
- Never add Claude as a co-author. No `Co-Authored-By` line in commits, no "Generated with Claude Code" in pull requests.

## File locations (changed 28 October 2026)

- The LSE OneDrive folder `C:\Users\joaov\OneDrive - London School of Economics` no longer exists.
- GitHub repositories are in `C:\Users\joaov\Documents\GitHub\<repo>`. Desktop, Documents and Pictures are in `C:\Users\joaov\`.
- All other former OneDrive folders (Doutorado, Projetinhos, Critical_Minerals and others) are in `G:\<same path>`. G: is Google Drive "My Drive", the same as `X:\My Drive`.
- Google Drive can keep files online-only. The first read downloads the file, which is slow for large data.
- Code and config paths were rewritten to the new locations on 28 October 2026.
- Logs, manifests, reports and other records of past runs keep the old paths. Do not rewrite them.
- If code still has an old path, map it: `OneDrive - London School of Economics\Documents\...` becomes `C:\Users\joaov\Documents\...`; any other `OneDrive - London School of Economics\<folder>\...` becomes `G:\<folder>\...`.
- Paths from other people's machines (for example `C:/Users/RASCHKA`, `C:/Users/fmuench`, `C:/Users/Joao`, `C:/Users/karol`) stay unchanged.

## LaTeX and PDF compilation

- Use an external LaTeX compiler, such as MiKTeX or TeX Live, to compile LaTeX documents to PDF.
- Do not use the Codex built-in PDF compiler. This instruction replaces earlier compiler instructions.
- Keep the existing LaTeX source editable. Delete generated auxiliary files after successful compilation.
