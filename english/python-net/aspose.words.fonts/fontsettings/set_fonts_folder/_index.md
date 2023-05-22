---
title: FontSettings.set_fonts_folder method
linktitle: set_fonts_folder method
articleTitle: set_fonts_folder method
second_title: Aspose.Words for Python
description: "FontSettings.set_fonts_folder method. Sets the folder where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts"
type: docs
weight: 80
url: /python-net/aspose.words.fonts/fontsettings/set_fonts_folder/
---

## set_fonts_folder(font_folder, recursive) {#str_bool}

Sets the folder where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts.
This is a shortcut to [FontSettings.set_fonts_folders()](../set_fonts_folders/#strlist_bool) for setting only one font directory.



```python
def set_fonts_folder(self, font_folder: str, recursive: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| font_folder | str |  |
| recursive | bool |  |

### Examples

Shows how to set a font source directory.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.name = "Arvo"
builder.writeln("Hello world!")
builder.font.name = "Amethysta"
builder.writeln("The quick brown fox jumps over the lazy dog.")

# Our font sources do not contain the font that we have used for text in this document.
# If we use these font settings while rendering this document,
# Aspose.Words will apply a fallback font to text which has a font that Aspose.Words cannot locate.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()

self.assertEqual(1, len(original_font_sources))
self.assertTrue(any(f for f in original_font_sources[0].get_available_fonts() if f.full_font_name == "Arial"))

# The default font sources are missing the two fonts that we are using in this document.
self.assertFalse(any(f for f in original_font_sources[0].get_available_fonts() if f.full_font_name == "Arvo"))
self.assertFalse(any(f for f in original_font_sources[0].get_available_fonts() if f.full_font_name == "Amethysta"))

# Use the "set_fonts_folder" method to set a directory which will act as a new font source.
# Pass "False" as the "recursive" argument to include fonts from all the font files that are in the directory
# that we are passing in the first argument, but not include any fonts in any of that directory's subfolders.
# Pass "True" as the "recursive" argument to include all font files in the directory that we are passing
# in the first argument, as well as all the fonts in its subdirectories.
aw.fonts.FontSettings.default_instance.set_fonts_folder(FONTS_DIR, recursive)

new_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()

self.assertEqual(1, len(new_font_sources))
self.assertFalse(any(f for f in new_font_sources[0].get_available_fonts() if f.full_font_name == "Arial"))
self.assertTrue(any(f for f in new_font_sources[0].get_available_fonts() if f.full_font_name == "Arvo"))

# The "Amethysta" font is in a subfolder of the font directory.
if recursive:
    self.assertEqual(25, len(new_font_sources[0].get_available_fonts()))
    self.assertTrue(any(f for f in new_font_sources[0].get_available_fonts() if f.full_font_name == "Amethysta"))
else:
    self.assertEqual(18, len(new_font_sources[0].get_available_fonts()))
    self.assertFalse(any(f for f in new_font_sources[0].get_available_fonts() if f.full_font_name == "Amethysta"))

doc.save(ARTIFACTS_DIR + "FontSettings.set_fonts_folder.pdf")

# Restore the original font sources.
aw.fonts.FontSettings.default_instance.set_fonts_sources(original_font_sources)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSettings](../)

