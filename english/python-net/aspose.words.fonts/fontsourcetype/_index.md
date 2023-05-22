---
title: FontSourceType enumeration
linktitle: FontSourceType enumeration
articleTitle: FontSourceType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FontSourceType enumeration. Specifies the type of a font source."
type: docs
weight: 160
url: /python-net/aspose.words.fonts/fontsourcetype/
---

## FontSourceType enumeration

Specifies the type of a font source.


### Members

| Name | Description |
| --- | --- |
| FONT_FILE | A [FileFontSource](../filefontsource/) object that represents single font file. |
| FONTS_FOLDER | A [FolderFontSource](../folderfontsource/) object that represents folder with font files. |
| MEMORY_FONT | A [MemoryFontSource](../memoryfontsource/) object that represents single font in memory. |
| SYSTEM_FONTS | A [SystemFontSource](../systemfontsource/) object that represents all fonts installed to the system. |
| FONT_STREAM | A [StreamFontSource](../streamfontsource/) object that represents a stream with font data. |

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

* module [aspose.words.fonts](../)

