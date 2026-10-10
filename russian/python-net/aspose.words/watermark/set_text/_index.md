---
title: Watermark.set_text method
linktitle: set_text method
articleTitle: set_text method
second_title: Aspose.Words for Python
description: "aspose.words.Watermark.set_text method"
type: docs
weight: 40
url: /ru/python-net/aspose.words/watermark/set_text/
---

## set_text(text) {#str}

Adds Text watermark into the document.


```python
def set_text(self, text: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | str | Text that is displayed as a watermark. |

### Remarks

The text length must be in the range from 1 to 200 inclusive.
The text cannot be ``None`` or contain only whitespaces.



### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throws when the text length is out of range or the text contains only whitespaces. |
| RuntimeError (Proxy error(ArgumentNullException)) | Throws when the text is ``None``. |

## set_text(text, options) {#str_textwatermarkoptions}

Adds Text watermark into the document.


```python
def set_text(self, text: str, options: aspose.words.TextWatermarkOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | str | Text that is displayed as a watermark. |
| options | [TextWatermarkOptions](../../textwatermarkoptions/) | Defines additional options for the text watermark. |

### Remarks

The text length must be in the range from 1 to 200 inclusive.
The text cannot be ``None`` or contain only whitespaces.



If [TextWatermarkOptions](../../textwatermarkoptions/) is ``None``, the watermark will be set with default options.


### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throws when the text length is out of range or the text contain only whitespaces. |
| RuntimeError (Proxy error(ArgumentNullException)) | Throws when the text is ``None``. |

## Examples

Shows how to create a text watermark.

```python
doc = aw.Document()
# Добавьте водяной знак в виде простого текста.
doc.watermark.set_text(text='Aspose Watermark')
# Если мы хотим изменить форматирование текста, используя его как водяной знак,
# мы можем сделать это, передав объект TextWatermarkOptions при создании водяного знака.
text_watermark_options = aw.TextWatermarkOptions()
text_watermark_options.font_family = 'Arial'
text_watermark_options.font_size = 36
text_watermark_options.color = aspose.pydrawing.Color.black
text_watermark_options.layout = aw.WatermarkLayout.DIAGONAL
text_watermark_options.is_semitrasparent = False
doc.watermark.set_text(text='Aspose Watermark', options=text_watermark_options)
doc.save(file_name=ARTIFACTS_DIR + 'Document.TextWatermark.docx')
# Мы можем удалить водяной знак из документа следующим образом.
if doc.watermark.type == aw.WatermarkType.TEXT:
    doc.watermark.remove()
```

## See Also

* module [aspose.words](../../)
* class [Watermark](../)

