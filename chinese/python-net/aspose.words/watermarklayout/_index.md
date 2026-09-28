---
title: WatermarkLayout enumeration
linktitle: WatermarkLayout enumeration
articleTitle: WatermarkLayout enumeration
second_title: Aspose.Words for Python
description: "aspose.words.WatermarkLayout enumeration. Defines layout of the watermark relative to the watermark center."
type: docs
weight: 1500
url: /zh/python-net/aspose.words/watermarklayout/
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
# 添加纯文本水印。
doc.watermark.set_text(text='Aspose Watermark')
# 如果我们希望将其用作水印来编辑文本格式，
# 我们可以在创建水印时传入 TextWatermarkOptions 对象来实现。
text_watermark_options = aw.TextWatermarkOptions()
text_watermark_options.font_family = 'Arial'
text_watermark_options.font_size = 36
text_watermark_options.color = aspose.pydrawing.Color.black
text_watermark_options.layout = aw.WatermarkLayout.DIAGONAL
text_watermark_options.is_semitrasparent = False
doc.watermark.set_text(text='Aspose Watermark', options=text_watermark_options)
doc.save(file_name=ARTIFACTS_DIR + 'Document.TextWatermark.docx')
# 我们可以这样从文档中移除水印。
if doc.watermark.type == aw.WatermarkType.TEXT:
    doc.watermark.remove()
```

### See Also

* module [aspose.words](../)

