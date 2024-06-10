---
title: EmbeddedFontStyle enumeration
linktitle: EmbeddedFontStyle enumeration
articleTitle: EmbeddedFontStyle enumeration
second_title: Aspose.Words for Python
description: "aspose.words.fonts.EmbeddedFontStyle enumeration. Specifies the style of an embedded font inside a [FontInfo](../fontinfo/) object."
type: docs
weight: 30
url: /python-net/aspose.words.fonts/embeddedfontstyle/
---

## EmbeddedFontStyle enumeration

Specifies the style of an embedded font inside a [FontInfo](../fontinfo/) object.



### Members

| Name | Description |
| --- | --- |
| REGULAR | Specifies the Regular embedded font. |
| BOLD | Specifies the Bold embedded font. |
| ITALIC | Specifies the Italic embedded font. |
| BOLD_ITALIC | Specifies the Bold-Italic embedded font. |

### Examples

Shows how to extract an embedded font from a document, and save it to the local file system.

```python
doc = aw.Document(MY_DIR + 'Embedded font.docx')
embedded_font = doc.font_infos.get_by_name('Alte DIN 1451 Mittelschrift')
embedded_font_bytes = embedded_font.get_embedded_font(aw.fonts.EmbeddedFontFormat.OPEN_TYPE, aw.fonts.EmbeddedFontStyle.REGULAR)
with open(ARTIFACTS_DIR + 'Alte DIN 1451 Mittelschrift.ttf', 'wb') as file:
    file.write(embedded_font_bytes)
# Embedded font formats may be different in other formats such as .doc.
# We need to know the correct format before we can extract the font.
doc = aw.Document(MY_DIR + 'Embedded font.doc')
self.assertIsNone(doc.font_infos.get_by_name('Alte DIN 1451 Mittelschrift').get_embedded_font(aw.fonts.EmbeddedFontFormat.OPEN_TYPE, aw.fonts.EmbeddedFontStyle.REGULAR))
self.assertIsNotNone(doc.font_infos.get_by_name('Alte DIN 1451 Mittelschrift').get_embedded_font(aw.fonts.EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, aw.fonts.EmbeddedFontStyle.REGULAR))
# Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
embedded_font_bytes = doc.font_infos.get_by_name('Alte DIN 1451 Mittelschrift').get_embedded_font_as_open_type(aw.fonts.EmbeddedFontStyle.REGULAR)
with open(ARTIFACTS_DIR + 'Alte DIN 1451 Mittelschrift.otf', 'wb') as file:
    file.write(embedded_font_bytes)
```

### See Also

* module [aspose.words.fonts](../)

