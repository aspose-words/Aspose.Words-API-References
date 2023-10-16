---
title: FileFontSource class
linktitle: FileFontSource class
articleTitle: FileFontSource class
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FileFontSource class. Represents the single TrueType font file stored in the file system"
type: docs
weight: 40
url: /python-net/aspose.words.fonts/filefontsource/
---

## FileFontSource class

Represents the single TrueType font file stored in the file system.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/python-net/working-with-fonts/) documentation article.




**Inheritance:** [FileFontSource](./) → [FontSourceBase](../fontsourcebase/)

### Constructors
| Name | Description |
| --- | --- |
| [FileFontSource(file_path)](./__init__/#str) | Ctor. |
| [FileFontSource(file_path, priority)](./__init__/#str_int) | Ctor. |
| [FileFontSource(file_path, priority, cache_key)](./__init__/#str_int_str) | Ctor. |

### Properties

| Name | Description |
| --- | --- |
| [cache_key](./cache_key/) | The key of this source in the cache. |
| [file_path](./file_path/) | Path to the font file. |
| [priority](../fontsourcebase/priority/) | Returns the font source priority.<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |
| [type](./type/) | Returns the type of the font source. |
| [warning_callback](../fontsourcebase/warning_callback/) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss.<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_available_fonts()](../fontsourcebase/get_available_fonts/#default) | Returns list of fonts available via this source.<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |

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
* class [FontSourceBase](../fontsourcebase/)

