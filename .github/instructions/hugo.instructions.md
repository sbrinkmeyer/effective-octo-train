# Hugo Development Instructions

Apply these rules whenever working on Hugo site implementation.

## Scope
- Content authoring in `content/`
- Site config in `hugo.toml`
- Theme-aware edits for `themes/hugo-universal-theme/`

## Rules
- Keep URL behavior stable unless migrations are explicitly requested.
- Respect existing taxonomies and menu structure.
- Use front matter fields already present in similar files whenever possible.
- Avoid introducing shortcodes or template functions not supported by the current Hugo version.
- For layout changes, prefer overrides in project-level layouts (if introduced) instead of modifying theme source directly.

## Quality checks
- Ensure new pages are discoverable via menu, section list, or taxonomy (as requested).
- Confirm no broken internal links.
- Keep copy edits and structural edits in separate commits when possible.
