---
title: ReflectionFormat.distance property
linktitle: distance property
articleTitle: distance property
second_title: Aspose.Words for Python
description: "ReflectionFormat.distance property. Gets or sets a double value that specifies the amount of separation of the reflected image from the object in points"
type: docs
weight: 20
url: /python-net/aspose.words.drawing/reflectionformat/distance/
---

## ReflectionFormat.distance property

Gets or sets a double value that specifies the amount of separation of the reflected image from the object in points.
The default value is 0.0.


```python
@property
def distance(self) -> float:
    ...

@distance.setter
def distance(self, value: float):
    ...

```

### Examples

Shows how to interact with reflection shape effect.

```python
doc = aw.Document(file_name=MY_DIR + "Various shapes.docx")
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
shape.reflection.transparency = 0.37
shape.reflection.size = 0.48
shape.reflection.blur = 17.5
shape.reflection.distance = 9.2
doc.save(file_name=ARTIFACTS_DIR + "Shape.Reflection.docx")
doc = aw.Document(file_name=ARTIFACTS_DIR + "Shape.Reflection.docx")
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

