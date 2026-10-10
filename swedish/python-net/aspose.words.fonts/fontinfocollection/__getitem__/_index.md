---
title: FontInfoCollection indexer
linktitle: FontInfoCollection indexer
articleTitle: FontInfoCollection indexer
second_title: Aspose.Words for Python
description: "FontInfoCollection indexer. Gets a font at the specified index."
type: docs
weight: 10
url: /sv/python-net/aspose.words.fonts/fontinfocollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Gets a font at the specified index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

Shows how to extract an embedded font from a document, and save it to the local file system.

```python
doc = aw.Document(file_name=MY_DIR + 'Embedded font.docx')
embedded_font = doc.font_infos.get_by_name('Alte DIN 1451 Mittelschrift')
embedded_font_bytes = embedded_font.get_embedded_font(aw.fonts.EmbeddedFontFormat.OPEN_TYPE, aw.fonts.EmbeddedFontStyle.REGULAR)
system_helper.io.File.write_all_bytes(ARTIFACTS_DIR + 'Alte DIN 1451 Mittelschrift.ttf', embedded_font_bytes)
# Inbäddade teckensnittformat kan vara olika i andra format som .doc.
# Vi måste känna till rätt format innan vi kan extrahera teckensnittet.
doc = aw.Document(file_name=MY_DIR + 'Embedded font.doc')
self.assertIsNone(doc.font_infos.get_by_name('Alte DIN 1451 Mittelschrift').get_embedded_font(aw.fonts.EmbeddedFontFormat.OPEN_TYPE, aw.fonts.EmbeddedFontStyle.REGULAR))
self.assertIsNotNone(doc.font_infos.get_by_name('Alte DIN 1451 Mittelschrift').get_embedded_font(aw.fonts.EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, aw.fonts.EmbeddedFontStyle.REGULAR))
# Vi kan också konvertera inbäddat OpenType-format, som kommer från .doc-dokument, till OpenType.
embedded_font_bytes = doc.font_infos.get_by_name('Alte DIN 1451 Mittelschrift').get_embedded_font_as_open_type(aw.fonts.EmbeddedFontStyle.REGULAR)
system_helper.io.File.write_all_bytes(ARTIFACTS_DIR + 'Alte DIN 1451 Mittelschrift.otf', embedded_font_bytes)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontInfoCollection](../)

