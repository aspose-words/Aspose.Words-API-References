---
title: Node.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "Node.remove method. Removes itself from the parent."
type: docs
weight: 490
url: /ar/python-net/aspose.words/node/remove/
---

## remove() {#default}

Removes itself from the parent.


```python
def remove(self):
    ...
```

### Examples

Shows how to delete all shapes with images from a document.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)
self.assertEqual(9, len(list(filter(lambda s: s.has_image, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(shapes))))))))
for shape in filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(shapes))):
    if shape.has_image:
        shape.remove()
self.assertEqual(0, len(list(filter(lambda s: s.has_image, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(shapes))))))))
```

Shows how to remove all child nodes of a specific type from a composite node.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
self.assertEqual(2, doc.get_child_nodes(aw.NodeType.TABLE, True).count)
cur_node = doc.first_section.body.first_child
while cur_node != None:
    # احفظ عقدة الأخ التالي كمتغير في حال أردنا الانتقال إليها بعد حذف هذه العقدة.
    next_node = cur_node.next_sibling
    # يمكن لجسم القسم أن يحتوي على عقد الفقرة والجدول.
    # إذا كانت العقدة جدولًا، احذفها من الأصل.
    if cur_node.node_type == aw.NodeType.TABLE:
        cur_node.remove()
    cur_node = next_node
self.assertEqual(0, doc.get_child_nodes(aw.NodeType.TABLE, True).count)
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

