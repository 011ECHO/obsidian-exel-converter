## What's new in v2.1

**Language selection splash screen**
- On first load, you now pick your language (English, Русский, Українська, Español) from a dedicated start screen before the converter appears.
- Default language is now English.

**Branding**
- The app is now named **Obsidian Exel Converter** — the header title is static across all languages instead of being translated.
- Browser tab title changed to **"OEC by ECHO"**.
- Added a favicon matching the app's logo (same table icon on a purple gradient background), embedded directly in the file — works fully offline, no external image request.
- `<html lang>` now updates automatically to match the selected language.

**Bug fixes & cleanup**
- Removed a stray unused CSS rule left over from an earlier draft.
- Removed the now-unused "title" translation key from all four language blocks.

**QA pass**
- Verified all four languages have matching translation keys (no missing strings).
- Verified HTML structure integrity (tag balance, no duplicate element IDs).
