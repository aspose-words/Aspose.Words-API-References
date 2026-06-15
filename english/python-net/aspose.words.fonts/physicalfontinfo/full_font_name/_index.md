---
title: PhysicalFontInfo.full_font_name property
linktitle: full_font_name property
articleTitle: full_font_name property
second_title: Aspose.Words for Python
description: "PhysicalFontInfo.full_font_name property. Full name of the font."
type: docs
weight: 40
url: /python-net/aspose.words.fonts/physicalfontinfo/full_font_name/
---

## PhysicalFontInfo.full_font_name property

Full name of the font.


```python
@property
def full_font_name(self) -> str:
    ...

```

### Examples

Shows how to list available fonts.

```python
# Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
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

