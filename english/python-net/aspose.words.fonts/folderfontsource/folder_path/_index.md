---
title: FolderFontSource.folder_path property
linktitle: folder_path property
articleTitle: folder_path property
second_title: Aspose.Words for Python
description: "FolderFontSource.folder_path property. Path to the folder."
type: docs
weight: 20
url: /python-net/aspose.words.fonts/folderfontsource/folder_path/
---

## FolderFontSource.folder_path property

Path to the folder.


```python
@property
def folder_path(self) -> str:
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

