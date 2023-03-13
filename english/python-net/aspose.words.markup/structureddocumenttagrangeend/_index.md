﻿---
title: StructuredDocumentTagRangeEnd class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents an end of ranged structured document tag which accepts multi-sections content"
type: docs
weight: 190
url: /python-net/aspose.words.markup/structureddocumenttagrangeend/
---

## StructuredDocumentTagRangeEnd class

Represents an end of **ranged** structured document tag which accepts multi-sections content.
See also [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/) node.
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/python-net/working-with-content-control-sdt/) documentation article.




Can be immediate child of [Body](../../aspose.words/body/) node **only**.



**Inheritance:** [StructuredDocumentTagRangeEnd](./) → [Node](../../aspose.words/node/)

### Constructors
| Name | Description |
| --- | --- |
| [StructuredDocumentTagRangeEnd(doc, id)](./__init__/#documentbase_int) | Initializes a new instance of the **Structured document tag range end** class. |

### Properties

| Name | Description |
| --- | --- |
| [custom_node_id](../../aspose.words/node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [id](./id/) | Specifies a unique read-only persistent numerical Id for this **StructuredDocumentTagRange** node. Corresponding [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/) node has the same [StructuredDocumentTagRangeStart.id](../structureddocumenttagrangestart/id/). |
| [is_composite](../../aspose.words/node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [next_sibling](../../aspose.words/node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [node_type](./node_type/) | Returns [NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END](../../aspose.words/nodetype/#STRUCTURED_DOCUMENT_TAG_RANGE_END). |
| [parent_node](../../aspose.words/node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [previous_sibling](../../aspose.words/node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ clone(is_clone_children)](../../aspose.words/node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#unknown) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_text()](../../aspose.words/node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ next_pre_order(root_node)](../../aspose.words/node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ node_type_to_string(node_type)](../../aspose.words/node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ previous_pre_order(root_node)](../../aspose.words/node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ to_string(save_format)](../../aspose.words/node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ to_string(save_options)](../../aspose.words/node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

### Examples

Shows how to get the properties of multi-section structured document tags.

```python
doc = aw.Document(MY_DIR + "Multi-section structured document tags.docx")

range_start_tag = doc.get_child_nodes(aw.NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, True)[0].as_structured_document_tag_range_start()
range_end_tag = doc.get_child_nodes(aw.NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, True)[0].as_structured_document_tag_range_end()


print("StructuredDocumentTagRangeStart values:")
print(f"\t|id: {range_start_tag.id}")
print(f"\t|title: {range_start_tag.title}")
print(f"\t|placeholder_name: {range_start_tag.placeholder_name}")
print(f"\t|is_showing_placeholder_text: {range_start_tag.is_showing_placeholder_text}")
print(f"\t|lock_content_control: {range_start_tag.lock_content_control}")
print(f"\t|lock_contents: {range_start_tag.lock_contents}")
print(f"\t|level: {range_start_tag.level}")
print(f"\t|node_type: {range_start_tag.node_type}")
print(f"\t|range_end: {range_start_tag.range_end}")
print(f"\t|color: {range_start_tag.color.to_argb()}")
print(f"\t|sdt_type: {range_start_tag.sdt_type}")
print(f"\t|flat_opc_content: {range_start_tag.word_open_xml}")
print(f"\t|tag: {range_start_tag.tag}\n")

print("StructuredDocumentTagRangeEnd values:")
print(f"\t|id: {range_end_tag.id}")
print(f"\t|node_type: {range_end_tag.node_type}")
```

### See Also

* module [aspose.words.markup](../)
* class [Node](../../aspose.words/node/)

