---
title: Shape.has_smart_art property
linktitle: has_smart_art property
articleTitle: has_smart_art property
second_title: Aspose.Words for Python
description: "Shape.has_smart_art property. Returns ``True`` if this [Shape](../) has a SmartArt object."
type: docs
weight: 90
url: /python-net/aspose.words.drawing/shape/has_smart_art/
---

## Shape.has_smart_art property

Returns ``True`` if this [Shape](../) has a SmartArt object.



```python
@property
def has_smart_art(self) -> bool:
    ...

```

### Examples

Shows how to count the number of shapes in a document with SmartArt objects.

```python
doc = aw.Document(MY_DIR + "SmartArt.docx")

number_of_smart_art_shapes = len([node for node in doc.get_child_nodes(aw.NodeType.SHAPE, True) if node.as_shape().has_smart_art])

self.assertEqual(2, number_of_smart_art_shapes)
```

### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)

