---
title: panose property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the PANOSE typeface classification number."
type: docs
weight: 60
url: /python-net/aspose.words.fonts/fontinfo/panose/
---

## FontInfo.panose property

Gets or sets the PANOSE typeface classification number.

PANOSE is a compact 10-byte description of a fonts critical visual characteristics, 
such as contrast, weight, and serif style. The digits represent Family Kind, Serif Style, 
Weight, Proportion, Contrast, Stroke Variation, Arm Style, Letterform, Midline, and X-Height.

Can be ``None``.




### Examples

Shows how to access and print details of each font in a document.

```python
doc = aw.Document(MY_DIR + "Document.docx")

for font_info in doc.font_infos:
    if font_info is not None:

        print("Font name: " + font_info.name)

        # Alt names are usually blank.
        print("Alt name:", font_info.alt_name)
        print("\t- Family:", font_info.family)
        print("\t-", ("Is TrueType" if font_info.is_true_type else "Is not TrueType"))
        print("\t- Pitch:", font_info.pitch)
        print("\t- Charset:", font_info.charset)
        print("\t- Panose:")
        print("\t\tFamily Kind:", font_info.panose[0])
        print("\t\tSerif Style:", font_info.panose[1])
        print("\t\tWeight:", font_info.panose[2])
        print("\t\tProportion:", font_info.panose[3])
        print("\t\tContrast:", font_info.panose[4])
        print("\t\tStroke Variation:", font_info.panose[5])
        print("\t\tArm Style:", font_info.panose[6])
        print("\t\tLetterform:", font_info.panose[7])
        print("\t\tMidline:", font_info.panose[8])
        print("\t\tX-Height:", font_info.panose[9])
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontInfo](../)

