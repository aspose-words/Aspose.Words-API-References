---
title: priority property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns the font source priority."
type: docs
weight: 10
url: /python-net/aspose.words.fonts/fontsourcebase/priority/
---

## FontSourceBase.priority property

Returns the font source priority.

This value is used when there are fonts with the same family name and style in different font sources.
In this case Aspose.Words selects the font from the source with the higher priority value.

The default value is 0.




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
* class [FontSourceBase](../)

