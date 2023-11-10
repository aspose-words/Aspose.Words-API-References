---
title: FileFontSource.file_path property
linktitle: file_path property
articleTitle: file_path property
second_title: Aspose.Words for Python
description: "FileFontSource.file_path property. Path to the font file."
type: docs
weight: 30
url: /python-net/aspose.words.fonts/filefontsource/file_path/
---

## FileFontSource.file_path property

Path to the font file.


```python
@property
def file_path(self) -> str:
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

