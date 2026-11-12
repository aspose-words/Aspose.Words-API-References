---
title: EmbeddedFontFormat enumeration
linktitle: EmbeddedFontFormat enumeration
articleTitle: EmbeddedFontFormat enumeration
second_title: Aspose.Words for Python
description: "aspose.words.fonts.EmbeddedFontFormat enumeration. Specifies format of particular embedded font inside [FontInfo](../fontinfo/) object."
type: docs
weight: 20
url: /tr/python-net/aspose.words.fonts/embeddedfontformat/
---

## EmbeddedFontFormat enumeration

Specifies format of particular embedded font inside [FontInfo](../fontinfo/) object.

When saving a document to a file, only embedded fonts of corresponding format are written down.




### Members

| Name | Description |
| --- | --- |
| EMBEDDED_OPEN_TYPE | Specifies Embedded OpenType (EOT) File Format. |
| OPEN_TYPE | Specifies font, embedded as plain copy of OpenType (TrueType) font file. |

### Examples

Shows how to extract an embedded font from a document, and save it to the local file system.

```python
doc = aw.Document(file_name=MY_DIR + 'Embedded font.docx')
embedded_font = doc.font_infos.get_by_name('Alte DIN 1451 Mittelschrift')
embedded_font_bytes = embedded_font.get_embedded_font(aw.fonts.EmbeddedFontFormat.OPEN_TYPE, aw.fonts.EmbeddedFontStyle.REGULAR)
system_helper.io.File.write_all_bytes(ARTIFACTS_DIR + 'Alte DIN 1451 Mittelschrift.ttf', embedded_font_bytes)
# Gömülü yazı tipi formatları .doc gibi diğer formatlarda farklı olabilir.
# Yazı tipini çıkarabilmemiz için doğru formatı bilmemiz gerekir.
doc = aw.Document(file_name=MY_DIR + 'Embedded font.doc')
self.assertIsNone(doc.font_infos.get_by_name('Alte DIN 1451 Mittelschrift').get_embedded_font(aw.fonts.EmbeddedFontFormat.OPEN_TYPE, aw.fonts.EmbeddedFontStyle.REGULAR))
self.assertIsNotNone(doc.font_infos.get_by_name('Alte DIN 1451 Mittelschrift').get_embedded_font(aw.fonts.EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, aw.fonts.EmbeddedFontStyle.REGULAR))
# Ayrıca, .doc belgelerinden gelen gömülü OpenType formatını OpenType'a dönüştürebiliriz.
embedded_font_bytes = doc.font_infos.get_by_name('Alte DIN 1451 Mittelschrift').get_embedded_font_as_open_type(aw.fonts.EmbeddedFontStyle.REGULAR)
system_helper.io.File.write_all_bytes(ARTIFACTS_DIR + 'Alte DIN 1451 Mittelschrift.otf', embedded_font_bytes)
```

### See Also

* module [aspose.words.fonts](../)

