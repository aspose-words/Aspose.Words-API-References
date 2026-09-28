---
title: FontSourceBase.get_available_fonts method
linktitle: get_available_fonts method
articleTitle: get_available_fonts method
second_title: Aspose.Words for Python
description: "FontSourceBase.get_available_fonts method. Returns list of fonts available via this source."
type: docs
weight: 90
url: /zh/python-net/aspose.words.fonts/fontsourcebase/get_available_fonts/
---

## get_available_fonts() {#default}

Returns list of fonts available via this source.


```python
def get_available_fonts(self):
    ...
```

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

* module [aspose.words.fonts](../../)
* class [FontSourceBase](../)

