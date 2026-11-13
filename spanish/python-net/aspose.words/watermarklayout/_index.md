---
title: WatermarkLayout enumeration
linktitle: WatermarkLayout enumeration
articleTitle: WatermarkLayout enumeration
second_title: Aspose.Words for Python
description: "aspose.words.WatermarkLayout enumeration. Defines layout of the watermark relative to the watermark center."
type: docs
weight: 1500
url: /es/python-net/aspose.words/watermarklayout/
---

## WatermarkLayout enumeration

Defines layout of the watermark relative to the watermark center.


### Members

| Name | Description |
| --- | --- |
| HORIZONTAL | Horizontal watermark layout. Corresponds to 0 degrees of rotation. |
| DIAGONAL | Diagonal watermark layout. Corresponds to 315 degrees of rotation. |

### Examples

Shows how to create a text watermark.

```python
doc = aw.Document()
# Agregar una marca de agua de texto plano.
doc.watermark.set_text(text='Aspose Watermark')
# Si deseamos editar el formato del texto usándolo como marca de agua,
# podemos hacerlo pasando un objeto TextWatermarkOptions al crear la marca de agua.
text_watermark_options = aw.TextWatermarkOptions()
text_watermark_options.font_family = 'Arial'
text_watermark_options.font_size = 36
text_watermark_options.color = aspose.pydrawing.Color.black
text_watermark_options.layout = aw.WatermarkLayout.DIAGONAL
text_watermark_options.is_semitrasparent = False
doc.watermark.set_text(text='Aspose Watermark', options=text_watermark_options)
doc.save(file_name=ARTIFACTS_DIR + 'Document.TextWatermark.docx')
# Podemos eliminar una marca de agua de un documento de esta manera.
if doc.watermark.type == aw.WatermarkType.TEXT:
    doc.watermark.remove()
```

### See Also

* module [aspose.words](../)

