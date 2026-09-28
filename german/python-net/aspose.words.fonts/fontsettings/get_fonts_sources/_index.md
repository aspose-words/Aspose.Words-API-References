---
title: FontSettings.get_fonts_sources method
linktitle: get_fonts_sources method
articleTitle: get_fonts_sources method
second_title: Aspose.Words for Python
description: "FontSettings.get_fonts_sources method. Gets a copy of the array that contains the list of sources where Aspose.Words looks for TrueType fonts."
type: docs
weight: 50
url: /de/python-net/aspose.words.fonts/fontsettings/get_fonts_sources/
---

## get_fonts_sources() {#default}

Gets a copy of the array that contains the list of sources where Aspose.Words looks for TrueType fonts.


```python
def get_fonts_sources(self):
    ...
```

### Remarks

The returned value is a copy of the data that Aspose.Words uses. If you change the entries
in the returned array, it will have no effect on document rendering. To specify new font sources
use the [FontSettings.set_fonts_sources()](../set_fonts_sources/#fontsourcebaselist) method.




### Returns

A copy of the current font sources.


### Examples

Shows how to add a font source to our existing font sources.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Amethysta'
builder.writeln('The quick brown fox jumps over the lazy dog.')
builder.font.name = 'Junction Light'
builder.writeln('The quick brown fox jumps over the lazy dog.')
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(original_font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in original_font_sources[0].get_available_fonts()]))
# Der Standard‑Schriftquelle fehlen zwei der Schriften, die wir in unserem Dokument verwenden.
# Wenn wir dieses Dokument speichern, wird Aspose.Words Ersatzschriften auf allen Text anwenden, der mit nicht zugänglichen Schriften formatiert ist.
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in original_font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Junction Light' for f in original_font_sources[0].get_available_fonts()]))
# Erstellen Sie eine Schriftquelle aus einem Ordner, der Schriften enthält.
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=True)
# Wenden Sie ein neues Array von Schriftquellen an, das die ursprünglichen Schriftquellen sowie unsere benutzerdefinierten Schriften enthält.
updated_font_sources = [original_font_sources[0], folder_font_source]
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=updated_font_sources)
# Verifizieren Sie, dass Aspose.Words Zugriff auf alle erforderlichen Schriften hat, bevor wir das Dokument zu PDF rendern.
updated_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertTrue(any([f.full_font_name == 'Arial' for f in updated_font_sources[0].get_available_fonts()]))
self.assertTrue(any([f.full_font_name == 'Amethysta' for f in updated_font_sources[1].get_available_fonts()]))
self.assertTrue(any([f.full_font_name == 'Junction Light' for f in updated_font_sources[1].get_available_fonts()]))
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.AddFontSource.pdf')
# Stellen Sie die ursprünglichen Schriftquellen wieder her.
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSettings](../)

