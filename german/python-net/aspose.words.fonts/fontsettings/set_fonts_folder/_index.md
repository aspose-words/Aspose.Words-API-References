---
title: FontSettings.set_fonts_folder method
linktitle: set_fonts_folder method
articleTitle: set_fonts_folder method
second_title: Aspose.Words for Python
description: "FontSettings.set_fonts_folder method. Sets the folder where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts"
type: docs
weight: 80
url: /de/python-net/aspose.words.fonts/fontsettings/set_fonts_folder/
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
| font_folder | str | The folder that contains TrueType fonts. |
| recursive | bool | True to scan the specified folders for fonts recursively. |

### Examples

Shows how to set a font source directory.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arvo'
builder.writeln('Hello world!')
builder.font.name = 'Amethysta'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# Unsere Schriftquellen enthalten nicht die Schrift, die wir für den Text in diesem Dokument verwendet haben.
# Wenn wir diese Schriftarteinstellungen beim Rendern dieses Dokuments verwenden,
# wird Aspose.Words eine Ersatzschrift auf Text anwenden, dessen Schrift von Aspose.Words nicht gefunden werden kann.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(original_font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in original_font_sources[0].get_available_fonts()]))
# In den Standard-Schriftquellen fehlen die beiden Schriften, die wir in diesem Dokument verwenden.
self.assertFalse(any([f.full_font_name == 'Arvo' for f in original_font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in original_font_sources[0].get_available_fonts()]))
# Verwenden Sie die Methode "SetFontsFolder", um ein Verzeichnis festzulegen, das als neue Schriftquelle dient.
# Übergeben Sie "false" als "recursive"-Argument, um Schriften aus allen Schriftdateien im Verzeichnis einzuschließen
# die wir im ersten Argument übergeben, jedoch keine Schriften in Unterordnern dieses Verzeichnisses einbeziehen.
# Übergeben Sie "true" als "recursive"-Argument, um alle Schriftdateien im Verzeichnis, das wir übergeben, einzuschließen
# im ersten Argument, sowie alle Schriften in dessen Unterverzeichnissen.
aw.fonts.FontSettings.default_instance.set_fonts_folder(FONTS_DIR, recursive)
new_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(new_font_sources))
self.assertFalse(any([f.full_font_name == 'Arial' for f in new_font_sources[0].get_available_fonts()]))
self.assertTrue(any([f.full_font_name == 'Arvo' for f in new_font_sources[0].get_available_fonts()]))
# Die Schrift "Amethysta" befindet sich in einem Unterordner des Schriftverzeichnisses.
if recursive:
    self.assertEqual(30, len(new_font_sources[0].get_available_fonts()))
    self.assertTrue(any([f.full_font_name == 'Amethysta' for f in new_font_sources[0].get_available_fonts()]))
else:
    self.assertEqual(18, len(new_font_sources[0].get_available_fonts()))
    self.assertFalse(any([f.full_font_name == 'Amethysta' for f in new_font_sources[0].get_available_fonts()]))
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.SetFontsFolder.pdf')
# Stellen Sie die ursprünglichen Schriftquellen wieder her.
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSettings](../)

