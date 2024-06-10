---
title: ReflectionFormat.size property
linktitle: size property
articleTitle: size property
second_title: Aspose.Words for Python
description: "ReflectionFormat.size property. Gets or sets a double value between 0.0 and 1.0 representing the size of the reflection as a percentage of the reflected object"
type: docs
weight: 30
url: /python-net/aspose.words.drawing/reflectionformat/size/
---

## ReflectionFormat.size property

Gets or sets a double value between 0.0 and 1.0 representing the size of the reflection
as a percentage of the reflected object.
The default value is 0.0.


```python
@property
def size(self) -> float:
    ...

@size.setter
def size(self, value: float):
    ...

```

### Examples

Shows how to interact with reflection shape effect.

```python
doc = aw.Document(file_name=MY_DIR + 'Various shapes.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
shape.reflection.transparency = 0.37
shape.reflection.size = 0.48
shape.reflection.blur = 17.5
shape.reflection.distance = 9.2
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Reflection.docx')
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Shape.Reflection.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
self.assertAlmostEqual(0.37, shape.reflection.transparency, delta=0.01)
self.assertAlmostEqual(0.48, shape.reflection.size, delta=0.01)
self.assertAlmostEqual(17.5, shape.reflection.blur, delta=0.01)
self.assertAlmostEqual(9.2, shape.reflection.distance, delta=0.01)
shape.reflection.remove()
self.assertEqual(0, shape.reflection.transparency)
self.assertEqual(0, shape.reflection.size)
self.assertEqual(0, shape.reflection.blur)
self.assertEqual(0, shape.reflection.distance)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ReflectionFormat](../)

