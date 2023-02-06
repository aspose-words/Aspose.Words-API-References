---
title: PhysicalFontInfo class
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies information about physical font available to Aspose.Words font engine"
type: docs
weight: 200
url: /python-net/aspose.words.fonts/physicalfontinfo/
---

## PhysicalFontInfo class

Specifies information about physical font available to Aspose.Words font engine.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/python-net/working-with-fonts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [file_path](./file_path/) | Path to the font file if any. |
| [font_family_name](./font_family_name/) | Family name of the font. |
| [full_font_name](./full_font_name/) | Full name of the font. |
| [version](./version/) | Version string of the font. |

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

* module [aspose.words.fonts](../)

