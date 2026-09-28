---
title: ShapeBase.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "ShapeBase.name property. Gets or sets the optional shape name."
type: docs
weight: 420
url: /zh/python-net/aspose.words.drawing/shapebase/name/
---

## ShapeBase.name property

Gets or sets the optional shape name.


```python
@property
def name(self) -> str:
    ...

@name.setter
def name(self, value: str):
    ...

```

### Remarks

Default is empty string.

Cannot be ``None``, but can be an empty string.




### Examples

Shows how to use a shape's alternative text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.CUBE, width=150, height=150)
shape.name = 'MyCube'
shape.alternative_text = 'Alt text for MyCube.'
# 我们可以通过右键单击形状，然后通过 "Format AutoShape" -> "Alt Text" 来访问形状的替代文本。
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AltText.docx')
# 将文档保存为 HTML，然后删除属于我们形状的链接图像。
# 读取我们 HTML 的浏览器将在缺失图像的位置显示 alt 文本。
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AltText.html')
os.unlink(ARTIFACTS_DIR + 'Shape.AltText.001.png')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

