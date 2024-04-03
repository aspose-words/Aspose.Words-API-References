---
title: ReflectionFormat.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "ReflectionFormat.remove method. Removes [ReflectionFormat](../) from the parent object."
type: docs
weight: 50
url: /python-net/aspose.words.drawing/reflectionformat/remove/
---

## remove() {#default}

Removes [ReflectionFormat](../) from the parent object.



```python
def remove(self):
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

