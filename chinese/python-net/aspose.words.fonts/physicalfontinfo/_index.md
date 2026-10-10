---
title: PhysicalFontInfo class
linktitle: PhysicalFontInfo class
articleTitle: PhysicalFontInfo class
second_title: Aspose.Words for Python
description: "aspose.words.fonts.PhysicalFontInfo class. Specifies information about physical font available to Aspose.Words font engine"
type: docs
weight: 220
url: /zh/python-net/aspose.words.fonts/physicalfontinfo/
---

## PhysicalFontInfo class

Specifies information about physical font available to Aspose.Words font engine.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/python-net/working-with-fonts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [embedding_licensing_rights](./embedding_licensing_rights/) | Embedding licensing rights for the font. |
| [file_path](./file_path/) | Path to the font file if any. |
| [font_family_name](./font_family_name/) | Family name of the font. |
| [full_font_name](./full_font_name/) | Full name of the font. |
| [version](./version/) | Version string of the font. |

### Examples

Shows how to list available fonts.

```python
# 配置 Aspose.Words 从自定义文件夹获取字体，然后打印所有可用的字体。
folder_font_source = [aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=True)]
for font_info in folder_font_source[0].get_available_fonts():
    print('FontFamilyName : {0}'.format(font_info.font_family_name))
    print('FullFontName  : {0}'.format(font_info.full_font_name))
    print('Version  : {0}'.format(font_info.version))
    print('FilePath : {0}\n'.format(font_info.file_path))
```

### See Also

* module [aspose.words.fonts](../)

