---
title: FontInfo.get_embedded_font_as_open_type method
linktitle: get_embedded_font_as_open_type method
articleTitle: get_embedded_font_as_open_type method
second_title: Aspose.Words for Python
description: "FontInfo.get_embedded_font_as_open_type method. Gets an embedded font file in OpenType format"
type: docs
weight: 100
url: /es/python-net/aspose.words.fonts/fontinfo/get_embedded_font_as_open_type/
---

## get_embedded_font_as_open_type(style) {#embeddedfontstyle}

Gets an embedded font file in OpenType format. Fonts in Embedded OpenType format are converted to OpenType.


```python
def get_embedded_font_as_open_type(self, style: aspose.words.fonts.EmbeddedFontStyle):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| style | [EmbeddedFontStyle](../../embeddedfontstyle/) | Specifies the font style to retrieve. |

### Returns

Returns ``None`` if the specified font is not embedded.


### Examples

Shows how to extract an embedded font from a document, and save it to the local file system.

```python
doc = aw.Document(file_name=MY_DIR + 'Embedded font.docx')
embedded_font = doc.font_infos.get_by_name('Alte DIN 1451 Mittelschrift')
embedded_font_bytes = embedded_font.get_embedded_font(aw.fonts.EmbeddedFontFormat.OPEN_TYPE, aw.fonts.EmbeddedFontStyle.REGULAR)
system_helper.io.File.write_all_bytes(ARTIFACTS_DIR + 'Alte DIN 1451 Mittelschrift.ttf', embedded_font_bytes)
# Los formatos de fuentes incrustadas pueden ser diferentes en otros formatos como .doc.
# Necesitamos conocer el formato correcto antes de poder extraer la fuente.
doc = aw.Document(file_name=MY_DIR + 'Embedded font.doc')
self.assertIsNone(doc.font_infos.get_by_name('Alte DIN 1451 Mittelschrift').get_embedded_font(aw.fonts.EmbeddedFontFormat.OPEN_TYPE, aw.fonts.EmbeddedFontStyle.REGULAR))
self.assertIsNotNone(doc.font_infos.get_by_name('Alte DIN 1451 Mittelschrift').get_embedded_font(aw.fonts.EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, aw.fonts.EmbeddedFontStyle.REGULAR))
# Además, podemos convertir el formato OpenType incrustado, que proviene de documentos .doc, a OpenType.
embedded_font_bytes = doc.font_infos.get_by_name('Alte DIN 1451 Mittelschrift').get_embedded_font_as_open_type(aw.fonts.EmbeddedFontStyle.REGULAR)
system_helper.io.File.write_all_bytes(ARTIFACTS_DIR + 'Alte DIN 1451 Mittelschrift.otf', embedded_font_bytes)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontInfo](../)

