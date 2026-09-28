---
title: TextWatermarkOptions.font_size property
linktitle: font_size property
articleTitle: font_size property
second_title: Aspose.Words for Python
description: "TextWatermarkOptions.font_size property. Gets or sets a font size"
type: docs
weight: 40
url: /ar/python-net/aspose.words/textwatermarkoptions/font_size/
---

## TextWatermarkOptions.font_size property

Gets or sets a font size. The default value is 0 - auto.


```python
@property
def font_size(self) -> float:
    ...

@font_size.setter
def font_size(self, value: float):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throws when argument was out of the range of valid values. |

### Remarks

Valid values range from 0 to 65.5 inclusive.

Auto font size means that the watermark will be scaled to its max width and max height relative to
the page margins.




### Examples

Shows how to create a text watermark.

```python
doc = aw.Document()
# أضف علامة مائية نصية عادية.
doc.watermark.set_text(text='Aspose Watermark')
# إذا أردنا تعديل تنسيق النص باستخدامه كعلامة مائية،
# يمكننا القيام بذلك بتمرير كائن TextWatermarkOptions عند إنشاء العلامة المائية.
text_watermark_options = aw.TextWatermarkOptions()
text_watermark_options.font_family = 'Arial'
text_watermark_options.font_size = 36
text_watermark_options.color = aspose.pydrawing.Color.black
text_watermark_options.layout = aw.WatermarkLayout.DIAGONAL
text_watermark_options.is_semitrasparent = False
doc.watermark.set_text(text='Aspose Watermark', options=text_watermark_options)
doc.save(file_name=ARTIFACTS_DIR + 'Document.TextWatermark.docx')
# يمكننا إزالة علامة مائية من مستند بهذه الطريقة.
if doc.watermark.type == aw.WatermarkType.TEXT:
    doc.watermark.remove()
```

### See Also

* module [aspose.words](../../)
* class [TextWatermarkOptions](../)

