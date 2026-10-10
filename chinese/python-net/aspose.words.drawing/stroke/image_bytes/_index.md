---
title: Stroke.image_bytes property
linktitle: image_bytes property
articleTitle: image_bytes property
second_title: Aspose.Words for Python
description: "Stroke.image_bytes property. Defines the image for a stroke image or pattern fill."
type: docs
weight: 160
url: /zh/python-net/aspose.words.drawing/stroke/image_bytes/
---

## Stroke.image_bytes property

Defines the image for a stroke image or pattern fill.


```python
@property
def image_bytes(self) -> bytes:
    ...

```

### Examples

Shows how to process shape stroke features.

```python
doc = aw.Document(file_name=MY_DIR + 'Shape stroke pattern border.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
stroke = shape.stroke
# 笔画可以有两种颜色，用于创建由双色图像数据定义的图案。
# 单色笔画不使用 Color2 属性。
self.assertEqual(aspose.pydrawing.Color.from_argb(255, 128, 0, 0), stroke.color)
self.assertEqual(aspose.pydrawing.Color.from_argb(255, 255, 255, 0), stroke.color2)
self.assertIsNotNone(stroke.image_bytes)
system_helper.io.File.write_all_bytes(ARTIFACTS_DIR + 'Drawing.StrokePattern.png', stroke.image_bytes)
```

### See Also

* module [aspose.words.drawing](../../)
* class [Stroke](../)

