---
title: TextWatermarkOptions.font_family property
linktitle: font_family property
articleTitle: font_family property
second_title: Aspose.Words for Python
description: "TextWatermarkOptions.font_family property. Gets or sets font family name"
type: docs
weight: 30
url: /tr/python-net/aspose.words/textwatermarkoptions/font_family/
---

## TextWatermarkOptions.font_family property

Gets or sets font family name. The default value is "Calibri".


```python
@property
def font_family(self) -> str:
    ...

@font_family.setter
def font_family(self, value: str):
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
* class [TextWatermarkOptions](../)

