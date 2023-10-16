---
title: FontSourceBase class
linktitle: FontSourceBase class
articleTitle: FontSourceBase class
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FontSourceBase class. This is an abstract base class for the classes that allow the user to specify various font sources"
type: docs
weight: 150
url: /python-net/aspose.words.fonts/fontsourcebase/
---

## FontSourceBase class

This is an abstract base class for the classes that allow the user to specify various font sources.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/python-net/working-with-fonts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [priority](./priority/) | Returns the font source priority. |
| [type](./type/) | Returns the type of the font source. |
| [warning_callback](./warning_callback/) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |

### Methods

| Name | Description |
| --- | --- |
|[ as_file_font_source()](./as_file_font_source/#default) | Cast [FontSourceBase](./) object to [FileFontSource](../filefontsource/). |
|[ as_folder_font_source()](./as_folder_font_source/#default) | Cast [FontSourceBase](./) object to [FolderFontSource](../folderfontsource/). |
|[ as_memory_font_source()](./as_memory_font_source/#default) | Cast [FontSourceBase](./) object to [MemoryFontSource](../memoryfontsource/). |
|[ as_stream_font_source()](./as_stream_font_source/#default) | Cast [FontSourceBase](./) object to [StreamFontSource](../streamfontsource/). |
|[ as_system_font_source()](./as_system_font_source/#default) | Cast [FontSourceBase](./) object to [SystemFontSource](../systemfontsource/). |
|[ get_available_fonts()](./get_available_fonts/#default) | Returns list of fonts available via this source. |

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

