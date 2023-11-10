---
title: FolderFontSource constructor
linktitle: FolderFontSource constructor
articleTitle: FolderFontSource constructor
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FolderFontSource constructor"
type: docs
weight: 10
url: /python-net/aspose.words.fonts/folderfontsource/__init__/
---

## FolderFontSource(folder_path, scan_subfolders) {#str_bool}

Ctor.


```python
def __init__(self, folder_path: str, scan_subfolders: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| folder_path | str | Path to folder. |
| scan_subfolders | bool | Determines whether or not to scan subfolders. |

## FolderFontSource(folder_path, scan_subfolders, priority) {#str_bool_int}

Ctor.


```python
def __init__(self, folder_path: str, scan_subfolders: bool, priority: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| folder_path | str | Path to folder. |
| scan_subfolders | bool | Determines whether or not to scan subfolders. |
| priority | int | Font source priority. See the [FontSourceBase.priority](../../fontsourcebase/priority/) property description for more information. |

## Examples

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

## See Also

* module [aspose.words.fonts](../../)
* class [FolderFontSource](../)

