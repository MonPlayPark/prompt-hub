# Prompt Hub V1 — M3 Initial Implementation

Local-first responsive PWA using IndexedDB; GitHub Pages target; JSON backup/restore; no login, cloud database, cloud sync, or Android Share Target in V1.

## Included in this first implementation slice
- Home, Prompt Library, Template Builder, Skill Library, Settings.
- Local create/edit/delete for prompts, templates, and skills.
- Prompt category, tags, favorites, and filtering/search.
- Template variables in `{{variable}}` syntax, copy and save-as-prompt.
- JSON backup/restore with schema version, basic validation, merge and replace modes.
- Persistent Storage request where supported; manifest and service worker shell cache.

## Known limitations / not release-ready yet
- This is an initial implementation slice, not a tested production release.
- Must run browser tests, especially backup/restore, before using for valuable data.
- JSON backups are not encrypted.
- URL import is not implemented yet; file `.md`/`.txt` import is also pending in this slice.
- Category management and formal schema migration tests are pending.
- Home quick search finds records but does not deep-link to a specific record.
- External Google Fonts require network; fallback fonts are present.
- PWA must be served via HTTPS or localhost; opening `index.html` with `file://` will not enable PWA features.

## Deploy to GitHub Pages
1. Create a repository named `prompt-hub`.
2. Upload the contents of this folder to the repository root (not the enclosing folder).
3. Repository Settings → Pages → deploy from `main` branch and `/ (root)`.
4. Wait for deployment, then open the HTTPS URL on desktop and Android.
5. Test create, reload, export, import, and cross-device restore before adding important data.

GitHub Pages on GitHub Free generally requires a public repository. The source will be public; never commit personal prompt data, backup files, or secrets.
