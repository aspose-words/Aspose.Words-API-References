---
title: FileFontSource.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "FileFontSource.type property. Returns the type of the font source."
type: docs
weight: 40
url: /python-net/aspose.words.fonts/filefontsource/type/
---

## FileFontSource.type property

Returns the type of the font source.


```python
@property
def type(self) -> aspose.words.fonts.FontSourceType:
    ...

```

### Examples

Shows how to use a font file in the local file system as a font source.

```python
file_font_source = aw.fonts.FileFontSource(MY_DIR + "Alte DIN 1451 Mittelschrift.ttf", 0)

doc = aw.Document()
doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.set_fonts_sources([file_font_source])

self.assertEqual(MY_DIR + "Alte DIN 1451 Mittelschrift.ttf", file_font_source.file_path)
self.assertEqual(aw.fonts.FontSourceType.FONT_FILE, file_font_source.type)
self.assertEqual(0, file_font_source.priority)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FileFontSource](../)

