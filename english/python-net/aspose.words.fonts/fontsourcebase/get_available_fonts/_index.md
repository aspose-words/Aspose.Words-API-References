---
title: FontSourceBase.get_available_fonts method
linktitle: get_available_fonts method
articleTitle: get_available_fonts method
second_title: Aspose.Words for Python
description: "FontSourceBase.get_available_fonts method. Returns list of fonts available via this source."
type: docs
weight: 90
url: /python-net/aspose.words.fonts/fontsourcebase/get_available_fonts/
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
* class [FontSourceBase](../)

