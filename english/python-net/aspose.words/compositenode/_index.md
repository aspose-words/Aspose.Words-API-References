﻿---
title: CompositeNode class
linktitle: CompositeNode class
articleTitle: CompositeNode class
second_title: Aspose.Words for Python
description: "aspose.words.CompositeNode class. Base class for nodes that can contain other nodes"
type: docs
weight: 210
url: /python-net/aspose.words/compositenode/
---

## CompositeNode class

Base class for nodes that can contain other nodes.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/python-net/aspose-words-document-object-model/) documentation article.




A document is represented as a tree of nodes, similar to DOM or XmlDocument.

For more info see the Composite design pattern.

The [CompositeNode](./) class:


* Provides access to the child nodes.
  
* Implements Composite operations such as insert and remove children.
  
* Provides methods for XPath navigation.
  



**Inheritance:** [CompositeNode](./) → [Node](../node/)

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of immediate children of this node. |
| [custom_node_id](../node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [first_child](./first_child/) | Gets the first child of the node. |
| [has_child_nodes](./has_child_nodes/) | Returns ``True`` if this node has any child nodes. |
| [is_composite](./is_composite/) | Returns ``True`` as this node can have child nodes. |
| [last_child](./last_child/) | Gets the last child of the node. |
| [next_sibling](../node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [node_type](../node/node_type/) | Gets the type of this node.<br>(Inherited from [Node](../node/)) |
| [parent_node](../node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [previous_sibling](../node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](../node/accept/#documentvisitor) | Accepts a visitor.<br>(Inherited from [Node](../node/)) |
|[ append_child(new_child)](./append_child/#node) | Adds the specified node to the end of the list of child nodes for this node. |
|[ clone(is_clone_children)](../node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../node/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#unknown) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../node/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ get_child(node_type, index, is_deep)](./get_child/#nodetype_int_bool) | Returns an Nth child node that matches the specified type. |
|[ get_child_nodes(node_type, is_deep)](./get_child_nodes/#nodetype_bool) | Returns a live collection of child nodes that match the specified type. |
|[ get_text()](./get_text/#default) | Gets the text of this node and of all its children. |
|[ index_of(child)](./index_of/#node) | Returns the index of the specified child node in the child node array. |
|[ insert_after(new_child, ref_child)](./insert_after/#node_node) | Inserts the specified node immediately after the specified reference node. |
|[ insert_before(new_child, ref_child)](./insert_before/#node_node) | Inserts the specified node immediately before the specified reference node. |
|[ next_pre_order(root_node)](../node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ node_type_to_string(node_type)](../node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../node/)) |
|[ prepend_child(new_child)](./prepend_child/#node) | Adds the specified node to the beginning of the list of child nodes for this node. |
|[ previous_pre_order(root_node)](../node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ remove()](../node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../node/)) |
|[ remove_all_children()](./remove_all_children/#default) | Removes all the child nodes of the current node. |
|[ remove_child(old_child)](./remove_child/#node) | Removes the specified child node. |
|[ remove_smart_tags()](./remove_smart_tags/#default) | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
|[ select_nodes(xpath)](./select_nodes/#str) | Selects a list of nodes matching the XPath expression. |
|[ select_single_node(xpath)](./select_single_node/#str) | Selects the first [Node](../node/) that matches the XPath expression. |
|[ to_string(save_format)](../node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ to_string(save_options)](../node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |

### Examples

Shows how to traverse through a composite node's collection of child nodes.

```python
doc = aw.Document()

# Add two runs and one shape as child nodes to the first paragraph of this document.
paragraph = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
paragraph.append_child(aw.Run(doc, "Hello world! "))

shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 200
shape.height = 200
# Note that the 'custom_node_id' is not saved to an output file and exists only during the node lifetime.
shape.custom_node_id = 100
shape.wrap_type = aw.drawing.WrapType.INLINE
paragraph.append_child(shape)

paragraph.append_child(aw.Run(doc, "Hello again!"))

# Iterate through the paragraph's collection of immediate children,
# and print any runs or shapes that we find within.
children = paragraph.get_child_nodes(aw.NodeType.ANY, False)

self.assertEqual(3, paragraph.get_child_nodes(aw.NodeType.ANY, False).count)

for child in children:
    if child.node_type == aw.NodeType.RUN:
        print("Run contents:")
        print(f"\t\"{child.get_text().strip()}\"")

    elif child.node_type == aw.NodeType.SHAPE:
        child_shape = child.as_shape()
        print("Shape:")
        print(f"\t{child_shape.shape_type}, {child_shape.width}x{child_shape.height}")
```

### See Also

* module [aspose.words](../)
* class [Node](../node/)

