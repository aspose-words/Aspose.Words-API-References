---
title: PhysicalFontInfo.version property
linktitle: version property
articleTitle: version property
second_title: Aspose.Words for Python
description: "PhysicalFontInfo.version property. Version string of the font."
type: docs
weight: 50
url: /python-net/aspose.words.fonts/physicalfontinfo/version/
---

## PhysicalFontInfo.version property

Version string of the font.


```python
@property
def version(self) -> str:
    ...

```

### Examples

Shows how to list available fonts.

```python
# Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
folder_font_source = [aw.fonts.FolderFontSource(FONTS_DIR, True)]
for font_info in folder_font_source[0].get_available_fonts():
    print('FontFamilyName :', font_info.font_family_name)
    print('FullFontName   :', font_info.full_font_name)
    print('Version  :', font_info.version)
    print('FilePath :', font_info.file_path)
    print()
```

### See Also

* module [aspose.words.fonts](../../)
* class [PhysicalFontInfo](../)

