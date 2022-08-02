---
title: name property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets the name of the font."
type: docs
weight: 50
url: /python-net/aspose.words.fonts/fontinfo/name/
---

## FontInfo.name property

Gets the name of the font.

Cannot be ``null``. Can be an empty string.




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

