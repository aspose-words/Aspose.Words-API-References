---
title: NodeCollection class
linktitle: NodeCollection class
articleTitle: NodeCollection class
second_title: Aspose.Words for Python
description: "aspose.words.NodeCollection class. Represents a collection of nodes of a specific type"
type: docs
weight: 770
url: /python-net/aspose.words/nodecollection/
---

## NodeCollection class

Represents a collection of nodes of a specific type.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/python-net/aspose-words-document-object-model/) documentation article.




### Remarks

[NodeCollection](./) does not own the nodes it contains, rather, is just a selection of nodes
of the specified type, but the nodes are stored in the tree under their respective parent nodes.

[NodeCollection](./) supports indexed access, iteration and provides add and remove methods.

The [NodeCollection](./) collection is "live", i.e. changes to the children of the node object
that it was created from are immediately reflected in the nodes returned by the [NodeCollection](./)
properties and methods.

[NodeCollection](./) is returned by [CompositeNode.get_child_nodes()](../compositenode/get_child_nodes/#nodetype_bool)
and also serves as a base class for typed node collections such as [SectionCollection](../sectioncollection/),
[ParagraphCollection](../paragraphcollection/) etc.

[NodeCollection](./) can be "flat" and contain only immediate children of the node it was created
from, or it can be "deep" and contain all descendant children.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Retrieves a node at the given index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of nodes in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ add(node)](./add/#node) | Adds a node to the end of the collection. |
|[ clear()](./clear/#default) | Removes all nodes from this collection and from the document. |
|[ contains(node)](./contains/#node) | Determines whether a node is in the collection. |
|[ index_of(node)](./index_of/#node) | Returns the zero-based index of the specified node. |
|[ insert(index, node)](./insert/#int_node) | Inserts a node into the collection at the specified index. |
|[ remove(node)](./remove/#node) | Removes the node from the collection and from the document. |
|[ remove_at(index)](./remove_at/#int) | Removes the node at the specified index from the collection and from the document. |
|[ to_array()](./to_array/#default) | Copies all nodes from the collection to a new array of nodes. |

### Examples

Shows how to replace all textbox shapes with image shapes.

```python
doc = aw.Document(file_name=MY_DIR + 'Textboxes in drawing canvas.docx')
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(3, len(list(filter(lambda s: s.shape_type == aw.drawing.ShapeType.TEXT_BOX, shapes))))
self.assertEqual(1, len(list(filter(lambda s: s.shape_type == aw.drawing.ShapeType.IMAGE, shapes))))
for shape in shapes:
    if shape.shape_type == aw.drawing.ShapeType.TEXT_BOX:
        replacement_shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.IMAGE)
        replacement_shape.image_data.set_image(file_name=IMAGE_DIR + 'Logo.jpg')
        replacement_shape.left = shape.left
        replacement_shape.top = shape.top
        replacement_shape.width = shape.width
        replacement_shape.height = shape.height
        replacement_shape.relative_horizontal_position = shape.relative_horizontal_position
        replacement_shape.relative_vertical_position = shape.relative_vertical_position
        replacement_shape.horizontal_alignment = shape.horizontal_alignment
        replacement_shape.vertical_alignment = shape.vertical_alignment
        replacement_shape.wrap_type = shape.wrap_type
        replacement_shape.wrap_side = shape.wrap_side
        shape.parent_node.insert_after(replacement_shape, shape)
        shape.remove()
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(0, len(list(filter(lambda s: s.shape_type == aw.drawing.ShapeType.TEXT_BOX, shapes))))
self.assertEqual(4, len(list(filter(lambda s: s.shape_type == aw.drawing.ShapeType.IMAGE, shapes))))
doc.save(file_name=ARTIFACTS_DIR + 'Shape.ReplaceTextboxesWithImages.docx')
```

### See Also

* module [aspose.words](../)

