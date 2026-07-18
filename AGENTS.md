# AGENTS.md

## Repository Scope

This repository contains static assets for `owbastion.com`. Work is limited to asset files, asset metadata, generation prompts, and configuration directly related to asset delivery. Do not implement website application logic, APIs, databases, or game logic here.

## Working Conventions

- Keep changes narrow and explicit; implement only what the request or the asset delivery workflow requires.
- Before editing, inspect relevant directories, existing asset names, references, and the Git worktree. Preserve unrelated uncommitted user changes.
- Place new assets in clear purpose-based directories and keep filenames stable. Avoid renaming referenced files without a specific reason.
- For binary asset changes, check dimensions, format, transparent edges, file size, and rendered appearance.
- Retain necessary source notes, generation prompts, or licensing information for generated assets. Do not commit third-party material with unknown provenance.
- Do not commit credentials, tokens, user data, build caches, editor temporary files, or unrelated large source files.
- Do not add dependencies, scripts, build systems, or directory layers unless the request or delivery workflow requires them.

## Verification

Run the smallest effective check for the type of change before submission:

- Documentation: check Markdown structure, paths, and examples.
- Images: confirm that files open correctly and check dimensions, format, transparency, and compression.
- SVG: confirm that the XML parses and contains no external network dependencies or embedded sensitive information.
- Delivery configuration: validate the configuration, then confirm reference paths and cache behavior.

If no automated check is available, state which manual checks were completed and which checks could not be run.

## Delivery Boundaries

- Do not publish externally, delete assets, modify the CDN, commit Git changes, or push to a remote by default.
- Before changing a live resource, deleting an asset, or overwriting an existing file, confirm the exact target and impact.
- At completion, report changed files, verification results, and any publishing steps that a maintainer must perform.
