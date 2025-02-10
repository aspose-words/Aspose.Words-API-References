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
| fonts_folders | List[str] | An array of folders that contain TrueType fonts. |
| recursive | bool | True to scan the specified folders for fonts recursively. |

### Remarks

By default, Aspose.Words looks for fonts installed to the system.

Setting this property resets the cache of all previously loaded fonts.




### Examples

Shows how to set multiple font source directories.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Amethysta'
builder.writeln('The quick brown fox jumps over the lazy dog.')
builder.font.name = 'Junction Light'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# Our font sources do not contain the font that we have used for text in this document.
# If we use these font settings while rendering this document,
# Aspose.Words will apply a fallback font to text which has a font that Aspose.Words cannot locate.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(original_font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in original_font_sources[0].get_available_fonts()]))
# The default font sources are missing the two fonts that we are using in this document.
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in original_font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Junction Light' for f in original_font_sources[0].get_available_fonts()]))
# Use the "SetFontsFolders" method to create a font source from each font directory that we pass as the first argument.
# Pass "false" as the "recursive" argument to include fonts from all the font files that are in the directories
# that we are passing in the first argument, but not include any fonts from any of the directories' subfolders.
# Pass "true" as the "recursive" argument to include all font files in the directories that we are passing
# in the first argument, as well as all the fonts in their subdirectories.
aw.fonts.FontSettings.default_instance.set_fonts_folders([FONTS_DIR + '/Amethysta', FONTS_DIR + '/Junction'], recursive)
new_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(2, len(new_font_sources))
self.assertFalse(any([f.full_font_name == 'Arial' for f in new_font_sources[0].get_available_fonts()]))
self.assertEqual(1, len(new_font_sources[0].get_available_fonts()))
self.assertTrue(any([f.full_font_name == 'Amethysta' for f in new_font_sources[0].get_available_fonts()]))
# The "Junction" folder itself contains no font files, but has subfolders that do.
if recursive:
    self.assertEqual(6, len(new_font_sources[1].get_available_fonts()))
    self.assertTrue(any([f.full_font_name == 'Junction Light' for f in new_font_sources[1].get_available_fonts()]))
else:
    self.assertEqual(0, len(new_font_sources[1].get_available_fonts()))
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.SetFontsFolders.pdf')
# Restore the original font sources.
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSettings](../)

