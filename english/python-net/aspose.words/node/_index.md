---
title: Node class
second_title: Aspose.Words for Python via .NET API Reference
description: "Base class for all nodes of a Word document."
type: docs
weight: 680
url: /python-net/aspose.words/node/
---

## Node class

Base class for all nodes of a Word document.


A document is represented as a tree of nodes, similar to DOM or XmlDocument.

For more info see the Composite design pattern.

The [Node](./) class:


* Defines the child node interface.
  
* Defines the interface for visiting nodes.
  
* Provides default cloning capability.
  
* Implements parent node and owner document mechanisms.
  
* Implements access to sibling nodes.
  



### Properties

| Name | Description |
| --- | --- |
| [custom_node_id](./custom_node_id/) | Specifies custom node identifier. |
| [document](./document/) | Gets the document to which this node belongs. |
| [is_composite](./is_composite/) | Returns true if this node can contain other nodes. |
| [next_sibling](./next_sibling/) | Gets the node immediately following this node. |
| [node_type](./node_type/) | Gets the type of this node. |
| [parent_node](./parent_node/) | Gets the immediate parent of this node. |
| [previous_sibling](./previous_sibling/) | Gets the node immediately preceding this node. |
| [range](./range/) | Returns a **Range** object that represents the portion of a document that is contained in this node. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ as_body()](./as_body/#default) |  |
|[ as_bookmark_end()](./as_bookmark_end/#default) |  |
|[ as_bookmark_start()](./as_bookmark_start/#default) |  |
|[ as_building_block()](./as_building_block/#default) |  |
|[ as_cell()](./as_cell/#default) |  |
|[ as_comment()](./as_comment/#default) |  |
|[ as_comment_range_end()](./as_comment_range_end/#default) |  |
|[ as_comment_range_start()](./as_comment_range_start/#default) |  |
|[ as_composite_node()](./as_composite_node/#default) |  |
|[ as_document()](./as_document/#default) |  |
|[ as_editable_range_end()](./as_editable_range_end/#default) |  |
|[ as_editable_range_start()](./as_editable_range_start/#default) |  |
|[ as_field_end()](./as_field_end/#default) |  |
|[ as_field_separator()](./as_field_separator/#default) |  |
|[ as_field_start()](./as_field_start/#default) |  |
|[ as_footnote()](./as_footnote/#default) |  |
|[ as_form_field()](./as_form_field/#default) |  |
|[ as_glossary_document()](./as_glossary_document/#default) |  |
|[ as_group_shape()](./as_group_shape/#default) |  |
|[ as_header_footer()](./as_header_footer/#default) |  |
|[ as_office_math()](./as_office_math/#default) |  |
|[ as_paragraph()](./as_paragraph/#default) |  |
|[ as_row()](./as_row/#default) |  |
|[ as_run()](./as_run/#default) |  |
|[ as_section()](./as_section/#default) |  |
|[ as_shape()](./as_shape/#default) |  |
|[ as_smart_tag()](./as_smart_tag/#default) |  |
|[ as_special_char()](./as_special_char/#default) |  |
|[ as_structured_document_tag()](./as_structured_document_tag/#default) |  |
|[ as_structured_document_tag_range_end()](./as_structured_document_tag_range_end/#default) |  |
|[ as_structured_document_tag_range_start()](./as_structured_document_tag_range_start/#default) |  |
|[ as_sub_document()](./as_sub_document/#default) |  |
|[ as_table()](./as_table/#default) |  |
|[ clone(is_clone_children)](./clone/#bool) | Creates a duplicate of the node. |
|[ get_ancestor(ancestor_type)](./get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/). |
|[ get_text()](./get_text/#default) | Gets the text of this node and of all its children. |
|[ next_pre_order(root_node)](./next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm. |
|[ node_type_to_string(node_type)](./node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string. |
|[ previous_pre_order(root_node)](./previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm. |
|[ remove()](./remove/#default) | Removes itself from the parent. |
|[ to_string(save_format)](./to_string/#saveformat) | Exports the content of the node into a string in the specified format. |
|[ to_string(save_options)](./to_string/#saveoptions) | Exports the content of the node into a string using the specified save options. |

### Examples

Shows how to clone a composite node.

```python
doc = aw.Document()
para = doc.first_section.body.first_paragraph
para.append_child(aw.Run(doc, "Hello world!"))

# Below are two ways of cloning a composite node.
# 1 -  Create a clone of a node, and create a clone of each of its child nodes as well.
clone_with_children = para.clone(True)

self.assertTrue(clone_with_children.as_composite_node().has_child_nodes)
self.assertEqual("Hello world!", clone_with_children.get_text().strip())

# 2 -  Create a clone of a node just by itself without any children.
clone_without_children = para.clone(False)

self.assertFalse(clone_without_children.as_composite_node().has_child_nodes)
self.assertEqual("", clone_without_children.get_text().strip())
```

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
children = paragraph.child_nodes

self.assertEqual(3, paragraph.child_nodes.count)

for child in children:
    if child.node_type == aw.NodeType.RUN:
        print("Run contents:")
        print(f"\t\"{child.get_text().strip()}\"")

    elif child.node_type == aw.NodeType.SHAPE:
        child_shape = child.as_shape()
        print("Shape:")
        print(f"\t{child_shape.shape_type}, {child_shape.width}x{child_shape.height}")
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

* module [aspose.words](../)

