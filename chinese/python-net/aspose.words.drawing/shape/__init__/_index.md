---
title: Shape constructor
linktitle: Shape constructor
articleTitle: Shape constructor
second_title: Aspose.Words for Python
description: "Shape constructor. Creates a new shape object."
type: docs
weight: 10
url: /zh/python-net/aspose.words.drawing/shape/__init__/
---

## Shape(doc, shape_type) {#documentbase_shapetype}

Creates a new shape object.


```python
def __init__(self, doc: aspose.words.DocumentBase, shape_type: aspose.words.drawing.ShapeType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../../aspose.words/documentbase/) | The owner document. |
| shape_type | [ShapeType](../../shapetype/) | The type of the shape to create. |

### Remarks

You should specify desired shape properties after you created a shape.




### Examples

Shows how to insert a shape with an image from the local file system into a document.

```python
doc = aw.Document()
# "Shape" 类的公共构造函数将创建一个使用 "ShapeMarkupLanguage.Vml" 标记类型的形状。
# 如果需要创建非基本类型的形状，例如 SingleCornerSnipped、TopCornersSnipped、DiagonalCornersSnipped，
# TopCornersOneRoundedOneSnipped、SingleCornerRounded、TopCornersRounded 或 DiagonalCornersRounded，
# 请使用 DocumentBuilder.InsertShape。
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.IMAGE)
shape.image_data.set_image(file_name=IMAGE_DIR + 'Windows MetaFile.wmf')
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
doc.save(file_name=ARTIFACTS_DIR + 'Image.FromFile.docx')
```

Shows how to create and format a text box.

```python
doc = aw.Document()
# 创建一个浮动文本框。
text_box = aw.drawing.Shape(doc, aw.drawing.ShapeType.TEXT_BOX)
text_box.wrap_type = aw.drawing.WrapType.NONE
text_box.height = 50
text_box.width = 200
# 设置形状内部文本的水平和垂直对齐方式。
text_box.horizontal_alignment = aw.drawing.HorizontalAlignment.CENTER
text_box.vertical_alignment = aw.drawing.VerticalAlignment.TOP
# 向文本框添加一个段落，并添加一段文本运行，文本框将显示该文本。
text_box.append_child(aw.Paragraph(doc))
para = text_box.first_paragraph
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
run = aw.Run(doc=doc)
run.text = 'Hello world!'
para.append_child(run)
doc.first_section.body.first_paragraph.append_child(text_box)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.CreateTextBox.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)

