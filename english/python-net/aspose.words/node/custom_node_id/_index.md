---
title: Node.custom_node_id property
linktitle: custom_node_id property
articleTitle: custom_node_id property
second_title: Aspose.Words for Python
description: "Node.custom_node_id property. Specifies custom node identifier."
type: docs
weight: 10
url: /python-net/aspose.words/node/custom_node_id/
---

## Node.custom_node_id property

Specifies custom node identifier.


```python
@property
def custom_node_id(self) -> int:
    ...

@custom_node_id.setter
def custom_node_id(self, value: int):
    ...

```

### Remarks

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.




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
* class [Node](../)

