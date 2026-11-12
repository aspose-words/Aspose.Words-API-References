---
title: Watermark.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "Watermark.remove method. Removes the watermark."
type: docs
weight: 20
url: /ru/python-net/aspose.words/watermark/remove/
---

## remove() {#default}

Removes the watermark.


```python
def remove(self):
    ...
```

### Examples

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

### See Also

* module [aspose.words](../../)
* class [Watermark](../)

