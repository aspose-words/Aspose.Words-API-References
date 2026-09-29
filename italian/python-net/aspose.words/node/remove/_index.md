---
title: Node.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "Node.remove method. Removes itself from the parent."
type: docs
weight: 490
url: /it/python-net/aspose.words/node/remove/
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
    # Salva il nodo fratello successivo come variabile nel caso volessimo spostarci su di esso dopo aver eliminato questo nodo.
    next_node = cur_node.next_sibling
    # Un corpo di sezione può contenere nodi Paragraph e Table.
    # Se il nodo è una Table, rimuovilo dal genitore.
    if cur_node.node_type == aw.NodeType.TABLE:
        cur_node.remove()
    cur_node = next_node
self.assertEqual(0, doc.get_child_nodes(aw.NodeType.TABLE, True).count)
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

