---
title: Watermark.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "Watermark.type property. Gets the watermark type."
type: docs
weight: 10
url: /tr/python-net/aspose.words/watermark/type/
---

## Watermark.type property

Gets the watermark type.


```python
@property
def type(self) -> aspose.words.WatermarkType:
    ...

```

### Examples

Shows how to create a text watermark.

```python
doc = aw.Document()
# Düz metin su işareti ekleyin.
doc.watermark.set_text(text='Aspose Watermark')
# Bunu su işareti olarak kullanarak metin biçimlendirmesini düzenlemek istersek,
# su işaretini oluştururken bir TextWatermarkOptions nesnesi geçirerek bunu yapabiliriz.
text_watermark_options = aw.TextWatermarkOptions()
text_watermark_options.font_family = 'Arial'
text_watermark_options.font_size = 36
text_watermark_options.color = aspose.pydrawing.Color.black
text_watermark_options.layout = aw.WatermarkLayout.DIAGONAL
text_watermark_options.is_semitrasparent = False
doc.watermark.set_text(text='Aspose Watermark', options=text_watermark_options)
doc.save(file_name=ARTIFACTS_DIR + 'Document.TextWatermark.docx')
# Bir belgeden su işaretini şu şekilde kaldırabiliriz.
if doc.watermark.type == aw.WatermarkType.TEXT:
    doc.watermark.remove()
```

### See Also

* module [aspose.words](../../)
* class [Watermark](../)

