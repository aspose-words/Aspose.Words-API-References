﻿---
title: CommentRangeEnd class
second_title: Aspose.Words for Python via .NET API Reference
description: "Denotes the end of a region of text that has a comment associated with it."
type: docs
weight: 180
url: /python-net/aspose.words/commentrangeend/
---

## CommentRangeEnd class

Denotes the end of a region of text that has a comment associated with it.


To create a comment anchored to a region of text, you need to create a [Comment](../comment/) and
then create [CommentRangeStart](../commentrangestart/) and [CommentRangeEnd](./) and set their identifiers 
to the same [Comment.id](../comment/id/) value.

[CommentRangeEnd](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).




**Inheritance:** [CommentRangeEnd](./) → [Node](../node/)

### Constructors
| Name | Description |
| --- | --- |
| [CommentRangeEnd(doc, id)](./__init__/#documentbase_int) | Initializes a new instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [custom_node_id](../node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [id](./id/) | Specifies the identifier of the comment to which this region is linked to. |
| [is_composite](../node/is_composite/) | Returns true if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [next_sibling](../node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [node_type](./node_type/) | Returns [NodeType.COMMENT_RANGE_END](../nodetype/#COMMENT_RANGE_END). |
| [parent_node](../node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [previous_sibling](../node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a **Range** object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ clone(is_clone_children)](../node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../node/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ get_text()](../node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../node/)) |
|[ next_pre_order(root_node)](../node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ node_type_to_string(node_type)](../node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../node/)) |
|[ previous_pre_order(root_node)](../node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ remove()](../node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../node/)) |
|[ to_string(save_format)](../node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ to_string(save_options)](../node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |

### See Also

* module [aspose.words](../)
* class [Node](../node/)
* class [Comment](../comment/)
* class [CommentRangeStart](../commentrangestart/)

