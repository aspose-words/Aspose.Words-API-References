---
title: FontSettings.set_fonts_folders method
linktitle: set_fonts_folders method
articleTitle: set_fonts_folders method
second_title: Aspose.Words for Python
description: "FontSettings.set_fonts_folders method. Sets the folders where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts."
type: docs
weight: 90
url: /python-net/aspose.words.fonts/fontsettings/set_fonts_folders/
---

## set_fonts_folders(fonts_folders, recursive) {#strlist_bool}

Sets the folders where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts.


```python
def set_fonts_folders(self, fonts_folders: List[str], recursive: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| fonts_folders | List[str] |  |
| recursive | bool |  |

By default, Aspose.Words looks for fonts installed to the system.

Setting this property resets the cache of all previously loaded fonts.




### Examples

Shows how to set multiple font source directories.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.name = "Amethysta"
builder.writeln("The quick brown fox jumps over the lazy dog.")
builder.font.name = "Junction Light"
builder.writeln("The quick brown fox jumps over the lazy dog.")

# Our font sources do not contain the font that we have used for text in this document.
# If we use these font settings while rendering this document,
# Aspose.Words will apply a fallback font to text which has a font that Aspose.Words cannot locate.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()

self.assertEqual(1, len(original_font_sources))
self.assertTrue(any(f for f in original_font_sources[0].get_available_fonts() if f.full_font_name == "Arial"))

# The default font sources are missing the two fonts that we are using in this document.
self.assertFalse(any(f for f in original_font_sources[0].get_available_fonts() if f.full_font_name == "Amethysta"))
self.assertFalse(any(f for f in original_font_sources[0].get_available_fonts() if f.full_font_name == "Junction Light"))

# Use the "set_fonts_folders" method to create a font source from each font directory that we pass as the first argument.
# Pass "False" as the "recursive" argument to include fonts from all the font files that are in the directories
# that we are passing in the first argument, but not include any fonts from any of the directories' subfolders.
# Pass "True" as the "recursive" argument to include all font files in the directories that we are passing
# in the first argument, as well as all the fonts in their subdirectories.
aw.fonts.FontSettings.default_instance.set_fonts_folders([FONTS_DIR + "/Amethysta", FONTS_DIR + "/Junction"], recursive)

new_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()

self.assertEqual(2, len(new_font_sources))
self.assertFalse(any(f for f in new_font_sources[0].get_available_fonts() if f.full_font_name == "Arial"))
self.assertEqual(1, len(new_font_sources[0].get_available_fonts()))
self.assertTrue(any(f for f in new_font_sources[0].get_available_fonts() if f.full_font_name == "Amethysta"))

# The "Junction" folder itself contains no font files, but has subfolders that do.
if recursive:
    self.assertEqual(6, len(new_font_sources[1].get_available_fonts()))
    self.assertTrue(any(f for f in new_font_sources[1].get_available_fonts() if f.full_font_name == "Junction Light"))
else:
    self.assertEqual(0, len(new_font_sources[1].get_available_fonts()))

doc.save(ARTIFACTS_DIR + "FontSettings.set_fonts_folders.pdf")

# Restore the original font sources.
aw.fonts.FontSettings.default_instance.set_fonts_sources(original_font_sources)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSettings](../)

