---
title: PhysicalFontInfo.font_family_name property
linktitle: font_family_name property
articleTitle: font_family_name property
second_title: Aspose.Words for Python
description: "PhysicalFontInfo.font_family_name property. Family name of the font."
type: docs
weight: 20
url: /python-net/aspose.words.fonts/physicalfontinfo/font_family_name/
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
# Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
folder_font_source = [aw.fonts.FolderFontSource(FONTS_DIR, True)]

for font_info in folder_font_source[0].get_available_fonts():
    print("FontFamilyName :", font_info.font_family_name)
    print("FullFontName   :", font_info.full_font_name)
    print("Version  :", font_info.version)
    print("FilePath :", font_info.file_path)
    print()
```

### See Also

* module [aspose.words.fonts](../../)
* class [PhysicalFontInfo](../)

