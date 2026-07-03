What's new in v2

Smarter link columns


Columns with mostly numeric values (prices, quantities, etc.) are now automatically excluded from the "Link columns [[...]]" list, since numeric values rarely repeat and used to create orphan nodes on the graph.


Table preview


After processing a table, you now see a preview of the first 3 rows before generating files, so you can confirm everything was parsed correctly.


XLSX support


Upload .xlsx / .xls files directly — no need to export to CSV first. If the workbook has multiple sheets, a sheet picker appears.


Drag & drop


Drop a .csv / .xlsx file straight onto the input area instead of using the upload button.


Auto-detection improvements


Delimiter detection now handles comma, semicolon, and tab automatically.
Encoding auto-detection (UTF-8 / Windows-1251) fixes garbled Cyrillic text from some Excel exports.


Properties-only mode


New toggle to generate notes with only frontmatter properties, skipping the title/table/notes body.


"Process a new table" bug fix


Fixed an issue where clicking this button wouldn't allow re-uploading the same file without a page reload.


Fixed back button


The step-2 back arrow was invisible for some users due to a font-loading issue — replaced with a reliable text character.


Much more detailed instructions


Step-by-step field-by-field guide for the JSON Importer dialog: which fields to fill in, which to leave untouched, and what "How to handle existing Notes" actually does.
Added a fallback path for installing JSON Importer via BRAT if it doesn't show up in plugin search.
Direct link to the JSON Importer GitHub page.


Localization fixes


Removed leftover Ukrainian strings from the Russian translation (template headers, example text).
