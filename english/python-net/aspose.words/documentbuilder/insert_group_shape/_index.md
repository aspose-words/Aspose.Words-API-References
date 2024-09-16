---
title: DocumentBuilder.insert_group_shape method
linktitle: insert_group_shape method
articleTitle: insert_group_shape method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_group_shape method"
type: docs
weight: 350
url: /python-net/aspose.words/documentbuilder/insert_group_shape/
---

## insert_group_shape(shapes) {#shapelist}

Groups the shapes passed as a parameter into a new GroupShape node which is inserted into the current position.


```python
def insert_group_shape(self, shapes: List[aspose.words.drawing.Shape]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| shapes | List[[Shape](../../../aspose.words.drawing/shape/)] | The list of shapes to be grouped. |

### Remarks

The position and dimension of the new GroupShape will be calculated automatically.

VML and DML shapes cannot be grouped together.




## insert_group_shape(left, top, width, height, shapes) {#float_float_float_float_shapelist}

Groups the shapes passed as a parameter into a new GroupShape node of the specified size which is inserted into the specified position.


```python
def insert_group_shape(self, left: float, top: float, width: float, height: float, shapes: List[aspose.words.drawing.Shape]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| left | float | Distance in points from the origin to the left side of the group shape. |
| top | float | Distance in points from the origin to the top side of the group shape. |
| width | float | The width of the group shape in points. A negative value is not allowed. |
| height | float | The height of the group shape in points. A negative value is not allowed. |
| shapes | List[[Shape](../../../aspose.words.drawing/shape/)] | The list of shapes to be grouped. |

### Remarks

VML and DML shapes cannot be grouped together.


## Examples

Shows how to insert DML group shape.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape1 = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=200, height=250)
shape1.left = 20
shape1.top = 20
shape1.stroke.color = aspose.pydrawing.Color.red
shape2 = builder.insert_shape(shape_type=aw.drawing.ShapeType.ELLIPSE, width=150, height=200)
shape2.left = 40
shape2.top = 50
shape2.stroke.color = aspose.pydrawing.Color.green
# Dimensions for the new GroupShape node.
left = 10
top = 10
width = 200
height = 300
# Insert GroupShape node for the specified size which is inserted into the specified position.
group_shape1 = builder.insert_group_shape(left=left, top=top, width=width, height=height, shapes=[shape1, shape2])
# Insert GroupShape node which position and dimension will be calculated automatically.
shape3 = shape1.clone(True).as_shape()
group_shape2 = builder.insert_group_shape(shapes=[shape3])
doc.save(file_name=ARTIFACTS_DIR + 'Shape.InsertGroupShape.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

