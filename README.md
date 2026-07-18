# owbastion.com Assets

`owbastion-assets` is the static asset repository for [owbastion.com](https://owbastion.com).
Assets may be consumed by the website and related services through a CDN, object storage, or deployment artifacts.
This repository does not contain application logic, APIs, or database code.

## Organization

Organize assets by purpose using clear, stable directories. For example:

```text
assets/
├── achievements/   # Achievement icons
├── heroes/         # Hero-related assets
├── maps/           # Map-related assets
└── branding/       # Logos, site icons, and brand assets
```

## Asset Conventions

- Use lowercase English letters, numbers, and hyphens for filenames. Preserve existing names for Chinese planning or generation documents when renaming would break references.
- Keep source files, publishable files, and previews separate so working files are not accidentally served as production assets.
- Prefer WebP or AVIF for published images, PNG when lossless transparency is required, and SVG for icons and logos where appropriate.
- Compress images before submission and check their dimensions, transparent edges, colors, and responsive rendering.
- Do not commit credentials, user data, build caches, editor temporary files, or large unprocessed source materials.

## Consumption

Consumers should use stable versioned paths or configured CDN URLs rather than local absolute paths.
When an asset changes, verify the consumer's cache policy and rendered output.

## Change Checklist

Before submitting a change, confirm that:

1. The file is in the correct purpose directory and follows the naming and format conventions.
2. The asset can be read by its consumer, with no unintended whitespace, borders, or transparency issues.
3. No credentials, private data, or unrelated generated output is included.
4. Documentation and directory structure remain consistent.
