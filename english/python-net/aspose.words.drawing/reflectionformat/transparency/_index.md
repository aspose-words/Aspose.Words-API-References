﻿---
title: ReflectionFormat.transparency property
linktitle: transparency property
articleTitle: transparency property
second_title: Aspose.Words for Python
description: "ReflectionFormat.transparency property. Gets or sets a double value between 0.0 (opaque) and 1.0 (clear) representing the degree of transparency for the reflection effect"
type: docs
weight: 40
url: /python-net/aspose.words.drawing/reflectionformat/transparency/
---

## ReflectionFormat.transparency property

Gets or sets a double value between 0.0 (opaque) and 1.0 (clear) representing the degree
of transparency for the reflection effect.
The default value is 0.0.


```python
@property
def transparency(self) -> float:
    ...

@transparency.setter
def transparency(self, value: float):
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
reflection_format = shape.reflection
self.assertAlmostEqual(0.37, reflection_format.transparency, delta=0.01)
self.assertAlmostEqual(0.48, reflection_format.size, delta=0.01)
self.assertAlmostEqual(17.5, reflection_format.blur, delta=0.01)
self.assertAlmostEqual(9.2, reflection_format.distance, delta=0.01)
reflection_format.remove()
self.assertEqual(0, reflection_format.transparency)
self.assertEqual(0, reflection_format.size)
self.assertEqual(0, reflection_format.blur)
self.assertEqual(0, reflection_format.distance)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ReflectionFormat](../)

