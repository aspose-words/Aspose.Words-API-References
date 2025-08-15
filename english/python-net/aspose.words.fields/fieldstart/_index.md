---
title: FieldStart class
linktitle: FieldStart class
articleTitle: FieldStart class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldStart class. Represents a start of a Word field in a document"
type: docs
weight: 970
url: /python-net/aspose.words.fields/fieldstart/
---

## FieldStart class

Represents a start of a Word field in a document.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

[FieldStart](./) is an inline-level node and represented by the
[ControlChar.FIELD_START_CHAR](../../aspose.words/controlchar/FIELD_START_CHAR/) control character in the document.

[FieldStart](./) can only be a child of [Paragraph](../../aspose.words/paragraph/).

A complete field in a Microsoft Word document is a complex structure consisting of
a field start character, field code, field separator character, field result
and field end character. Some fields only have field start, field code and field end.

To easily insert a new field into a document, use the [DocumentBuilder.insert_field()](../../aspose.words/documentbuilder/insert_field/#str)
method.




**Inheritance:** [FieldStart](./) → [FieldChar](../fieldchar/) → [SpecialChar](../../aspose.words/specialchar/) → [Inline](../../aspose.words/inline/) → [Node](../../aspose.words/node/)

### Properties

| Name | Description |
| --- | --- |
| [custom_node_id](../../aspose.words/node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [field_data](./field_data/) | Gets custom field data which is associated with the field. |
| [field_type](../fieldchar/field_type/) | Returns the type of the field.<br>(Inherited from [FieldChar](../fieldchar/)) |
| [font](../../aspose.words/inline/font/) | Provides access to the font formatting of this object.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [is_composite](../../aspose.words/node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [is_delete_revision](../../aspose.words/inline/is_delete_revision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [is_dirty](../fieldchar/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [FieldChar](../fieldchar/)) |
| [is_format_revision](../../aspose.words/inline/is_format_revision/) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [is_insert_revision](../../aspose.words/inline/is_insert_revision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [is_locked](../fieldchar/is_locked/) | Gets or sets whether the parent field is locked (should not recalculate its result).<br>(Inherited from [FieldChar](../fieldchar/)) |
| [is_move_from_revision](../../aspose.words/inline/is_move_from_revision/) | Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [is_move_to_revision](../../aspose.words/inline/is_move_to_revision/) | Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [next_sibling](../../aspose.words/node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [node_type](./node_type/) | Returns [NodeType.FIELD_START](../../aspose.words/nodetype/#FIELD_START). |
| [parent_node](../../aspose.words/node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [parent_paragraph](../../aspose.words/inline/parent_paragraph/) | Retrieves the parent [Paragraph](../../aspose.words/paragraph/) of this node.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [previous_sibling](../../aspose.words/node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ clone(is_clone_children)](../../aspose.words/node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#object) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_field()](../fieldchar/get_field/#default) | Returns a field for the field char.<br>(Inherited from [FieldChar](../fieldchar/)) |
|[ get_text()](../../aspose.words/node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ next_pre_order(root_node)](../../aspose.words/node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ node_type_to_string(node_type)](../../aspose.words/node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ previous_pre_order(root_node)](../../aspose.words/node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ to_string(save_format)](../../aspose.words/node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ to_string(save_options)](../../aspose.words/node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

### See Also

* module [aspose.words.fields](../)
* class [FieldChar](../fieldchar/)

