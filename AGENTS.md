# Repository Guidelines

## Project Structure & Module Organization
- Root holds source documents (e.g., `SAR EC Final GPGN.md`, PDFs) and folders like `portalDoc/`, `SAR EC Final GPGN_artifacts/`, and `New2016_17/`.
- Place supportive media in the closest `..._artifacts/` or subfolder next to the primary document. Keep relative paths stable.
- Prefer adding new images under a local `images/` folder near the Markdown file that references them.

## Build, Test, and Development Commands
- Preview Markdown: open in your editor or run `open "<file>.md"` (macOS) to launch default viewer.
- Search repository: `rg "keyword" -n` to locate references across docs.
- List structure: `ls -la` in directories to review newly added assets.

## Coding Style & Naming Conventions
- Markdown: use ATX headers (`#`, `##`), `-` for lists, fenced code blocks for snippets.
- Line width: wrap around 100 characters where practical; keep tables readable.
- Filenames: use kebab-case for new Markdown (`yyyy-topic.md`) and `images/topic-01.jpg`; avoid spaces.
- Keep original names for externally sourced PDFs but place them in an appropriate folder.

## Testing Guidelines
- Validate links and images by previewing Markdown; ensure relative paths resolve (e.g., `images/figure-01.jpg`).
- Run quick checks: `rg "\\[(.+)\\]\\((.+)\\)" -n` to spot link targets; `rg "TODO|FIXME" -n` to catch placeholders.
- For large diffs, attach a brief summary of what changed and why.

## Commit & Pull Request Guidelines
- Commits: concise, imperative mood. Example: `docs: add section on stakeholder meetings` or `assets: compress images for SAR EC`.
- PRs: include purpose, scope of files touched, and before/after notes if visuals changed. Link any related issue.
- Keep PRs focused (one document or topic). Prefer separate PRs for large media updates.

## Security & Configuration Tips
- Do not commit PII or sensitive internal data.
- For large binaries (>10 MB), coordinate on using Git LFS or provide external links if appropriate.
