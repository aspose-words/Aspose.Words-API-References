﻿---
title: MemoryFontSource class
linktitle: MemoryFontSource class
articleTitle: MemoryFontSource class
second_title: Aspose.Words for Python
description: "aspose.words.fonts.MemoryFontSource class. Represents the single TrueType font file stored in memory"
type: docs
weight: 210
url: /python-net/aspose.words.fonts/memoryfontsource/
---

## MemoryFontSource class

Represents the single TrueType font file stored in memory.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/python-net/working-with-fonts/) documentation article.




**Inheritance:** [MemoryFontSource](./) → [FontSourceBase](../fontsourcebase/)

### Constructors
| Name | Description |
| --- | --- |
| [MemoryFontSource(font_data)](./__init__/#bytes) | Ctor. |
| [MemoryFontSource(font_data, priority)](./__init__/#bytes_int) | Ctor. |
| [MemoryFontSource(font_data, priority, cache_key)](./__init__/#bytes_int_str) | Ctor. |

### Properties

| Name | Description |
| --- | --- |
| [cache_key](./cache_key/) | The key of this source in the cache. |
| [font_data](./font_data/) | Binary font data. |
| [priority](../fontsourcebase/priority/) | Returns the font source priority.<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |
| [type](./type/) | Returns the type of the font source. |
| [warning_callback](../fontsourcebase/warning_callback/) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss.<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_available_fonts()](../fontsourcebase/get_available_fonts/#default) | Returns list of fonts available via this source.<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |

### Examples

Shows how to use a byte array with data from a font file as a font source.

```python
font_bytes = system_helper.io.File.read_all_bytes(MY_DIR + 'Alte DIN 1451 Mittelschrift.ttf')
memory_font_source = aw.fonts.MemoryFontSource(font_data=font_bytes, priority=0)
doc = aw.Document()
doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.set_fonts_sources(sources=[memory_font_source])
self.assertEqual(aw.fonts.FontSourceType.MEMORY_FONT, memory_font_source.type)
self.assertEqual(0, memory_font_source.priority)
```

### See Also

* module [aspose.words.fonts](../)
* class [FontSourceBase](../fontsourcebase/)

