---
title: FootnoteSeparator class
linktitle: FootnoteSeparator class
articleTitle: FootnoteSeparator class
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteSeparator class. Represents a container for the footnote/endnote separator and continuation content of a document."
type: docs
weight: 70
url: /python-net/aspose.words.notes/footnoteseparator/
---

## FootnoteSeparator class

Represents a container for the footnote/endnote separator and continuation content of a document.


### Remarks

[FootnoteSeparator](./) can contain [Paragraph](../../aspose.words/paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

There can only be one [FootnoteSeparator](./) of each [FootnoteSeparatorType](../footnoteseparatortype/) in a document.




**Inheritance:** [FootnoteSeparator](./) → [Story](../../aspose.words/story/) → [CompositeNode](../../aspose.words/compositenode/) → [Node](../../aspose.words/node/)

### Properties

| Name | Description |
| --- | --- |
| [count](../../aspose.words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [custom_node_id](../../aspose.words/node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [first_child](../../aspose.words/compositenode/first_child/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [first_paragraph](../../aspose.words/story/first_paragraph/) | Gets the first paragraph in the story.<br>(Inherited from [Story](../../aspose.words/story/)) |
| [has_child_nodes](../../aspose.words/compositenode/has_child_nodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [is_composite](../../aspose.words/node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [last_child](../../aspose.words/compositenode/last_child/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [last_paragraph](../../aspose.words/story/last_paragraph/) | Gets the last paragraph in the story.<br>(Inherited from [Story](../../aspose.words/story/)) |
| [next_sibling](../../aspose.words/node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [node_type](../../aspose.words/node/node_type/) | Gets the type of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [paragraphs](../../aspose.words/story/paragraphs/) | Gets a collection of paragraphs that are immediate children of the story.<br>(Inherited from [Story](../../aspose.words/story/)) |
| [parent_node](../../aspose.words/node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [previous_sibling](../../aspose.words/node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [separator_type](./separator_type/) |  |
| [story_type](../../aspose.words/story/story_type/) | Gets the type of this story.<br>(Inherited from [Story](../../aspose.words/story/)) |
| [tables](../../aspose.words/story/tables/) | Gets a collection of tables that are immediate children of the story.<br>(Inherited from [Story](../../aspose.words/story/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](../../aspose.words/node/accept/#documentvisitor) | Accepts a visitor.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ accept_end(visitor)](../../aspose.words/compositenode/accept_end/#documentvisitor) | When implemented in a derived class, calls the VisitXXXEnd method of the specified document visitor.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ accept_start(visitor)](../../aspose.words/compositenode/accept_start/#documentvisitor) | When implemented in a derived class, calls the VisitXXXStart method of the specified document visitor.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ append_child(new_child)](../../aspose.words/compositenode/append_child/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ append_paragraph(text)](../../aspose.words/story/append_paragraph/#str) | A shortcut method that creates a [Paragraph](../../aspose.words/paragraph/) object with optional text and appends it to the end of this object.<br>(Inherited from [Story](../../aspose.words/story/)) |
|[ clone(is_clone_children)](../../aspose.words/node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ delete_shapes()](../../aspose.words/story/delete_shapes/#default) | Deletes all shapes from the text of this story.<br>(Inherited from [Story](../../aspose.words/story/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#object) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_child(node_type, index, is_deep)](../../aspose.words/compositenode/get_child/#nodetype_int_bool) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_child_nodes(node_type, is_deep)](../../aspose.words/compositenode/get_child_nodes/#nodetype_bool) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_text()](../../aspose.words/node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ index_of(child)](../../aspose.words/compositenode/index_of/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insert_after(new_child, ref_child)](../../aspose.words/compositenode/insert_after/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insert_before(new_child, ref_child)](../../aspose.words/compositenode/insert_before/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ next_pre_order(root_node)](../../aspose.words/node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ node_type_to_string(node_type)](../../aspose.words/node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ prepend_child(new_child)](../../aspose.words/compositenode/prepend_child/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ previous_pre_order(root_node)](../../aspose.words/node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove_all_children()](../../aspose.words/compositenode/remove_all_children/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ remove_child(old_child)](../../aspose.words/compositenode/remove_child/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ remove_smart_tags()](../../aspose.words/compositenode/remove_smart_tags/#default) | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ select_nodes(xpath)](../../aspose.words/compositenode/select_nodes/#str) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ select_single_node(xpath)](../../aspose.words/compositenode/select_single_node/#str) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ to_string(save_format)](../../aspose.words/node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ to_string(save_options)](../../aspose.words/node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

### Examples

Shows how to manage footnote separator format.

```python
doc = aw.Document(file_name=MY_DIR + 'Footnotes and endnotes.docx')
footnote_separator = doc.footnote_separators.get_by_footnote_separator_type(aw.notes.FootnoteSeparatorType.FOOTNOTE_SEPARATOR)
# Align footnote separator.
footnote_separator.first_paragraph.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
```

### See Also

* module [aspose.words.notes](../)
* class [Story](../../aspose.words/story/)

