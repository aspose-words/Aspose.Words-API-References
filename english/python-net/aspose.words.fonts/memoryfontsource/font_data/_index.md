---
title: font_data property
second_title: Aspose.Words for Python via .NET API Reference
description: "Binary font data."
type: docs
weight: 30
url: /python-net/aspose.words.fonts/memoryfontsource/font_data/
---

## MemoryFontSource.font_data property

Binary font data.


### Examples

Shows how to use a byte array with data from a font file as a font source.

```python
with open(MY_DIR + "Alte DIN 1451 Mittelschrift.ttf", "rb") as file:
    font_bytes = file.read()

memory_font_source = aw.fonts.MemoryFontSource(font_bytes, 0)

doc = aw.Document()
doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.set_fonts_sources([memory_font_source])

self.assertEqual(aw.fonts.FontSourceType.MEMORY_FONT, memory_font_source.type)
self.assertEqual(0, memory_font_source.priority)
```

### See Also

* module [aspose.words.fonts](../../)
* class [MemoryFontSource](../)

