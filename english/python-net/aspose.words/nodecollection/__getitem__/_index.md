---
title: NodeCollection indexer
linktitle: NodeCollection indexer
articleTitle: NodeCollection indexer
second_title: Aspose.Words for Python
description: "NodeCollection indexer. Retrieves a node at the given index."
type: docs
weight: 10
url: /python-net/aspose.words/nodecollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Retrieves a node at the given index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection of nodes. |

### Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. 
For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.




### Examples

Shows how to traverse through a composite node's collection of child nodes.

```python
doc = aw.Document()
# Add two runs and one shape as child nodes to the first paragraph of this document.
paragraph = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
paragraph.append_child(aw.Run(doc, 'Hello world! '))
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 200
shape.height = 200
# Note that the 'custom_node_id' is not saved to an output file and exists only during the node lifetime.
shape.custom_node_id = 100
shape.wrap_type = aw.drawing.WrapType.INLINE
paragraph.append_child(shape)
paragraph.append_child(aw.Run(doc, 'Hello again!'))
# Iterate through the paragraph's collection of immediate children,
# and print any runs or shapes that we find within.
children = paragraph.get_child_nodes(aw.NodeType.ANY, False)
self.assertEqual(3, paragraph.get_child_nodes(aw.NodeType.ANY, False).count)
for child in children:
    if child.node_type == aw.NodeType.RUN:
        print('Run contents:')
        print(f'\t"{child.get_text().strip()}"')
    elif child.node_type == aw.NodeType.SHAPE:
        child_shape = child.as_shape()
        print('Shape:')
        print(f'\t{child_shape.shape_type}, {child_shape.width}x{child_shape.height}')
```

### See Also

* module [aspose.words](../../)
* class [NodeCollection](../)

