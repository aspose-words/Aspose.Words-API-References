---
title: file_path property
second_title: Aspose.Words for Python via .NET API Reference
description: "Path to the font file if any."
type: docs
weight: 10
url: /python-net/aspose.words.fonts/physicalfontinfo/file_path/
---

## PhysicalFontInfo.file_path property

Path to the font file if any.


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

