# Obsidian Exel Converter

A browser-based tool that turns Excel/CSV/XLSX tables into Obsidian notes — with automatic graph connections via tags and `[[links]]`. No server, no install, no coding. Just open the HTML file.

**by 011ECHO**

---

## What it does

Got a spreadsheet — a client list, a supplier list, a contact database, anything with rows and columns — and want each row to become its own note in Obsidian, linked together on the graph? This tool generates the two files you need (a data `.csv` and a Handlebars `.md` template) for Obsidian's **JSON Importer** plugin to do the rest.

## Features

- 📋 **Multiple input methods** — paste with `Ctrl+V`, drag & drop a file, or upload with the button
- 📊 **Excel support** - upload `.xlsx` / `.xls` directly, no manual CSV export needed; picks up multiple sheets automatically
- 🌐 **Smart parsing** - auto-detects the delimiter (comma, semicolon, or tab) and the file encoding (UTF-8 / Windows-1251), so garbled Cyrillic text from Excel exports isn't a problem
- 🔍 **Live preview** - see the first rows of your table before generating anything
- 🏷️ **Tags** — add one or more tags so notes of the same category connect to each other on Obsidian's graph
- 🔗 **Link columns `[[...]]`** - turn any column into a real Obsidian link; every note sharing the same value connects automatically. Numeric columns (prices, quantities) are automatically excluded from this list, since they rarely repeat and would otherwise clutter the graph with orphan nodes
- 🧹 **Auto-sanitized column names** - spaces, dots, and commas in your spreadsheet headers are automatically converted into safe technical field names, so you never have to touch Handlebars syntax
- 📝 **Properties-only mode** - optionally generate notes with just frontmatter, no title/table/notes body
- 🈺 **4 languages** - English, Русский, Українська, Español
- 🔒 **100% local** - runs entirely in your browser; nothing is uploaded anywhere

## How to use

1. Open `index.html` in any modern browser
2. Pick your language on the start screen
3. Paste, drag, or upload your table
4. Click **Process table** — check the column preview and technical names
5. Choose which column becomes the note title
6. Optionally check off link columns and/or add tags
7. Click **Generate files** and download both — the CSV and the `.md` template
8. In Obsidian, install the [**JSON Importer**](https://github.com/farling42/obsidian-import-json) plugin (Community Plugins → Browse)
   - If it doesn't show up in search, install [**BRAT**](https://github.com/TfTHacker/obsidian42-brat) instead and add `https://github.com/farling42/obsidian-import-json` as a beta plugin
9. Open the importer, select your CSV and template, and fill in the fields as shown in the app's built-in instructions

Full field-by-field walkthrough of the importer dialog is included inside the tool itself (the "How to use this" panel at the top).

## Why this exists

Handlebars templates and CSV encoding quirks (spaces in column names, stray commas, Windows-1251 vs UTF-8) are a common source of failed imports. This tool removes that friction — you never touch the template syntax directly, and the technical column names are generated for you automatically.

## Tech

Single self-contained HTML file — vanilla JavaScript, [SheetJS](https://github.com/SheetJS/sheetjs) for `.xlsx` parsing, [Tabler Icons](https://tabler.io/icons) and Google Fonts (Inter, JetBrains Mono) for the UI. No build step, no dependencies to install.

## License

Free to use, modify, and share.
