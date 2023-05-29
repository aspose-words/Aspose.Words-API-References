---
title: Node.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "Node.remove method. Removes itself from the parent."
type: docs
weight: 490
url: /python-net/aspose.words/node/remove/
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
doc = aw.Document(MY_DIR + "Images.docx")
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)

self.assertEqual(9, len([node for node in shapes if node.as_shape().has_image]))

for node in shapes:
    shape = node.as_shape()
    if shape.has_image:
        shape.remove()

self.assertEqual(0, len([node for node in shapes if node.as_shape().has_image]))
```

Shows how to remove all child nodes of a specific type from a composite node.

```python
doc = aw.Document(MY_DIR + "Tables.docx")

self.assertEqual(2, doc.get_child_nodes(aw.NodeType.TABLE, True).count)

cur_node = doc.first_section.body.first_child

while cur_node is not None:

    # Save the next sibling node as a variable in case we want to move to it after deleting this node.
    next_node = cur_node.next_sibling

    # A section body can contain Paragraph and Table nodes.
    # If the node is a Table, remove it from the parent.
    if cur_node.node_type == aw.NodeType.TABLE:
        cur_node.remove()

    cur_node = next_node

self.assertEqual(0, doc.get_child_nodes(aw.NodeType.TABLE, True).count)
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

