---
title: PageSetup.page_width property
linktitle: page_width property
articleTitle: page_width property
second_title: Aspose.Words for Python
description: "PageSetup.page_width property. Returns or sets the width of the page in points."
type: docs
weight: 340
url: /zh/python-net/aspose.words/pagesetup/page_width/
---

## PageSetup.page_width property

Returns or sets the width of the page in points.


```python
@property
def page_width(self) -> float:
    ...

@page_width.setter
def page_width(self, value: float):
    ...

```

### Examples

Shows how to insert an image, and use it as a watermark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 将图像插入页眉，使其在每页可见。
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
shape.wrap_type = aw.drawing.WrapType.NONE
shape.behind_text = True
# 将图像放置在页面中心。
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.left = (builder.page_setup.page_width - shape.width) / 2
shape.top = (builder.page_setup.page_height - shape.height) / 2
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertWatermark.docx')
```

Shows how to insert a floating image, and specify its position and size.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
shape.wrap_type = aw.drawing.WrapType.NONE
# 配置形状的 \"RelativeHorizontalPosition\" 属性，以将 \"Left\" 属性的值视为形状的水平距离。
# 作为形状相对于页面左侧的水平距离，单位为点。
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
# 将形状相对于页面左侧的水平距离设置为 100。
shape.left = 100
# 以类似方式使用 \"RelativeVerticalPosition\" 属性，将形状定位在页面顶部下方 80pt。
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.top = 80
# 设置形状的高度，宽度将自动按比例缩放以保持尺寸。
shape.height = 125
self.assertEqual(125, shape.width)
# \"Bottom\" 和 \"Right\" 属性包含图像的底部和右侧边缘。
self.assertEqual(shape.top + shape.height, shape.bottom)
self.assertEqual(shape.left + shape.width, shape.right)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateFloatingPositionSize.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

