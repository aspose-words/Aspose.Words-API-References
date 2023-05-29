---
title: SystemFontSource.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "SystemFontSource.type property. Returns the type of the font source."
type: docs
weight: 20
url: /python-net/aspose.words.fonts/systemfontsource/type/
---

## SystemFontSource.type property

Returns the type of the font source.


### Examples

Shows how to access a document's system font source and set font substitutes.

```python
doc = aw.Document()
doc.font_settings = aw.fonts.FontSettings()

# By default, a blank document always contains a system font source.
self.assertEqual(1, len(doc.font_settings.get_fonts_sources()))

system_font_source = doc.font_settings.get_fonts_sources()[0]
self.assertEqual(aw.fonts.FontSourceType.SYSTEM_FONTS, system_font_source.type)
self.assertEqual(0, system_font_source.priority)

if platform.system() == "Windows":
    fonts_path = "C:\\WINDOWS\\Fonts"
    self.assertEqual(fonts_path.lower(), aw.fonts.SystemFontSource.get_system_font_folders()[0].lower())

for system_font_folder in aw.fonts.SystemFontSource.get_system_font_folders():

    print(system_font_folder)

# Set a font that exists in the Windows Fonts directory as a substitute for one that does not.
doc.font_settings.substitution_settings.font_info_substitution.enabled = True
doc.font_settings.substitution_settings.table_substitution.add_substitutes("Kreon-Regular", ["Calibri"])

self.assertEqual(1, len(list(doc.font_settings.substitution_settings.table_substitution.get_substitutes("Kreon-Regular"))))
self.assertIn("Calibri", list(doc.font_settings.substitution_settings.table_substitution.get_substitutes("Kreon-Regular")))

# Alternatively, we could add a folder font source in which the corresponding folder contains the font.
folder_font_source = aw.fonts.FolderFontSource(FONTS_DIR, False)
doc.font_settings.set_fonts_sources([system_font_source, folder_font_source])
self.assertEqual(2, len(doc.font_settings.get_fonts_sources()))

# Resetting the font sources still leaves us with the system font source as well as our substitutes.
doc.font_settings.reset_font_sources()

self.assertEqual(1, len(doc.font_settings.get_fonts_sources()))
self.assertEqual(aw.fonts.FontSourceType.SYSTEM_FONTS, doc.font_settings.get_fonts_sources()[0].type)
self.assertEqual(1, len(list(doc.font_settings.substitution_settings.table_substitution.get_substitutes("Kreon-Regular"))))
```

### See Also

* module [aspose.words.fonts](../../)
* class [SystemFontSource](../)

