---
title: PhysicalFontInfo.font_family_name property
linktitle: font_family_name property
articleTitle: font_family_name property
second_title: Aspose.Words for Python
description: "PhysicalFontInfo.font_family_name property. Family name of the font."
type: docs
weight: 30
url: /ru/python-net/aspose.words.fonts/physicalfontinfo/font_family_name/
---

## PhysicalFontInfo.font_family_name property

Family name of the font.


```python
@property
def font_family_name(self) -> str:
    ...

```

### Examples

Shows how to list available fonts.

```python
# Настройте Aspose.Words для получения шрифтов из пользовательской папки, а затем выведите каждый доступный шрифт.
folder_font_source = [aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=True)]
for font_info in folder_font_source[0].get_available_fonts():
    print('FontFamilyName : {0}'.format(font_info.font_family_name))
    print('FullFontName  : {0}'.format(font_info.full_font_name))
    print('Version  : {0}'.format(font_info.version))
    print('FilePath : {0}\n'.format(font_info.file_path))
```

### See Also

* module [aspose.words.fonts](../../)
* class [PhysicalFontInfo](../)

