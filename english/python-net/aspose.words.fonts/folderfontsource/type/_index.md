---
title: FolderFontSource.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "FolderFontSource.type property. Returns the type of the font source."
type: docs
weight: 40
url: /python-net/aspose.words.fonts/folderfontsource/type/
---

## FolderFontSource.type property

Returns the type of the font source.


```python
@property
def type(self) -> aspose.words.fonts.FontSourceType:
    ...

```

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

* module [aspose.words.fonts](../../)
* class [FolderFontSource](../)

