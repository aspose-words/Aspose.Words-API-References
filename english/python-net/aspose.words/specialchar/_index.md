---
title: SpecialChar class
linktitle: SpecialChar class
articleTitle: SpecialChar class
second_title: Aspose.Words for Python
description: "aspose.words.SpecialChar class. Base class for special characters in the document"
type: docs
weight: 1110
url: /python-net/aspose.words/specialchar/
---

## SpecialChar class

Base class for special characters in the document.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/python-net/aspose-words-document-object-model/) documentation article.




### Remarks

A Microsoft Word document can include a number of special characters
that represent fields, form fields, shapes, OLE objects, footnotes etc. For the list
of special characters see [ControlChar](../controlchar/).

[SpecialChar](./) is an inline-node and can only be a child of [Paragraph](../paragraph/).

[SpecialChar](./) char is used as a base class for more specific classes
that represent special characters that Aspose.Words provides programmatic access for.
The [SpecialChar](./) class is also used itself to represent special character for which
Aspose.Words does not provide detailed programmatic access.




**Inheritance:** [SpecialChar](./) → [Inline](../inline/) → [Node](../node/)

### Properties

| Name | Description |
| --- | --- |
| [custom_node_id](../node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [font](../inline/font/) | Provides access to the font formatting of this object.<br>(Inherited from [Inline](../inline/)) |
| [is_composite](../node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [is_delete_revision](../inline/is_delete_revision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../inline/)) |
| [is_format_revision](../inline/is_format_revision/) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../inline/)) |
| [is_insert_revision](../inline/is_insert_revision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../inline/)) |
| [is_move_from_revision](../inline/is_move_from_revision/) | Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../inline/)) |
| [is_move_to_revision](../inline/is_move_to_revision/) | Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../inline/)) |
| [next_sibling](../node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [node_type](./node_type/) | Returns [NodeType.SPECIAL_CHAR](../nodetype/#SPECIAL_CHAR). |
| [parent_node](../node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [parent_paragraph](../inline/parent_paragraph/) | Retrieves the parent [Paragraph](../paragraph/) of this node.<br>(Inherited from [Inline](../inline/)) |
| [previous_sibling](../node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ clone(is_clone_children)](../node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../node/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#object) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../node/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ get_text()](./get_text/#default) | Gets the special character that this node represents. |
|[ next_pre_order(root_node)](../node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ node_type_to_string(node_type)](../node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../node/)) |
|[ previous_pre_order(root_node)](../node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ remove()](../node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../node/)) |
|[ to_string(save_format)](../node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ to_string(save_options)](../node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |

### See Also

* module [aspose.words](../)
* class [Inline](../inline/)

