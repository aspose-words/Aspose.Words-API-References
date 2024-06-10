---
title: FontFamily enumeration
linktitle: FontFamily enumeration
articleTitle: FontFamily enumeration
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FontFamily enumeration. Represents the font family."
type: docs
weight: 80
url: /python-net/aspose.words.fonts/fontfamily/
---

## FontFamily enumeration

Represents the font family.

A font family is a set of fonts having common stroke width and serif characteristics.




### Members

| Name | Description |
| --- | --- |
| AUTO | Specifies a generic family name. This name is used when information about a font  does not exist or does not matter. The default font is used. |
| ROMAN | Specifies a proportional font with serifs. An example is Times New Roman. |
| SWISS | Specifies a proportional font without serifs. An example is Arial. |
| MODERN | Specifies a monospace font with or without serifs. Monospace fonts are  usually modern; examples include Pica, Elite, and Courier New. |
| SCRIPT | Specifies a font that is designed to look like handwriting; examples include Script and Cursive. |
| DECORATIVE | Specifies a novelty font. An example is Old English. |

### Examples

Shows how to access and print details of each font in a document.

```python
doc = aw.Document(MY_DIR + 'Document.docx')
for font_info in doc.font_infos:
    if font_info is not None:
        print('Font name: ' + font_info.name)
        # Alt names are usually blank.
        print('Alt name:', font_info.alt_name)
        print('\t- Family:', font_info.family)
        print('\t-', 'Is TrueType' if font_info.is_true_type else 'Is not TrueType')
        print('\t- Pitch:', font_info.pitch)
        print('\t- Charset:', font_info.charset)
        print('\t- Panose:')
        print('\t\tFamily Kind:', font_info.panose[0])
        print('\t\tSerif Style:', font_info.panose[1])
        print('\t\tWeight:', font_info.panose[2])
        print('\t\tProportion:', font_info.panose[3])
        print('\t\tContrast:', font_info.panose[4])
        print('\t\tStroke Variation:', font_info.panose[5])
        print('\t\tArm Style:', font_info.panose[6])
        print('\t\tLetterform:', font_info.panose[7])
        print('\t\tMidline:', font_info.panose[8])
        print('\t\tX-Height:', font_info.panose[9])
```

### See Also

* module [aspose.words.fonts](../)

