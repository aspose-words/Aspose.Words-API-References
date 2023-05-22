---
title: FontInfo.is_true_type property
linktitle: is_true_type property
articleTitle: is_true_type property
second_title: Aspose.Words for Python
description: "FontInfo.is_true_type property. Indicates that this font is a TrueType or OpenType font as opposed to a raster or vector font"
type: docs
weight: 40
url: /python-net/aspose.words.fonts/fontinfo/is_true_type/
---

## FontInfo.is_true_type property

Indicates that this font is a TrueType or OpenType font as opposed to a raster or vector font.
Default is ``True``.



### Examples

Shows how to print the details of what fonts are present in a document.

```python
doc = aw.Document(MY_DIR + "Embedded font.docx")

all_fonts = doc.font_infos

# Print all the used and unused fonts in the document.
for i in range(all_fonts.count):
    print(f"Font index #{i}")
    print(f"\tName: {all_fonts[i].name}")
    print(f'\tIs {"" if all_fonts[i].is_true_type else "not "}a TrueType font')
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontInfo](../)

