---
title: FolderFontSource class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents the folder that contains TrueType font files"
type: docs
weight: 50
url: /python-net/aspose.words.fonts/folderfontsource/
---

## FolderFontSource class

Represents the folder that contains TrueType font files.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/python-net/working-with-fonts/) documentation article.




**Inheritance:** [FolderFontSource](./) → [FontSourceBase](../fontsourcebase/)

### Constructors
| Name | Description |
| --- | --- |
| [FolderFontSource(folder_path, scan_subfolders)](./__init__/#str_bool) | Ctor. |
| [FolderFontSource(folder_path, scan_subfolders, priority)](./__init__/#str_bool_int) | Ctor. |

### Properties

| Name | Description |
| --- | --- |
| [folder_path](./folder_path/) | Path to the folder. |
| [priority](../fontsourcebase/priority/) | Returns the font source priority.<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |
| [scan_subfolders](./scan_subfolders/) | Determines whether or not to scan the subfolders. |
| [type](./type/) | Returns the type of the font source. |
| [warning_callback](../fontsourcebase/warning_callback/) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss.<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_available_fonts()](../fontsourcebase/get_available_fonts/#default) | Returns list of fonts available via this source.<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |

### Examples

Shows how to use a local system folder which contains fonts as a font source.

```python
# Create a font source from a folder that contains font files.
folder_font_source = aw.fonts.FolderFontSource(FONTS_DIR, False, 1)

doc = aw.Document()
doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.set_fonts_sources([folder_font_source])

self.assertEqual(FONTS_DIR, folder_font_source.folder_path)
self.assertEqual(False, folder_font_source.scan_subfolders)
self.assertEqual(aw.fonts.FontSourceType.FONTS_FOLDER, folder_font_source.type)
self.assertEqual(1, folder_font_source.priority)
```

### See Also

* module [aspose.words.fonts](../)
* class [FontSourceBase](../fontsourcebase/)

