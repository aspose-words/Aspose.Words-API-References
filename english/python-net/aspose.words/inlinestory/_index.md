---
title: InlineStory class
second_title: Aspose.Words for Python via .NET API Reference
description: "Base class for inline-level nodes that can contain paragraphs and tables."
type: docs
weight: 580
url: /python-net/aspose.words/inlinestory/
---

## InlineStory class

Base class for inline-level nodes that can contain paragraphs and tables.


**InlineStory** is a container for block-level nodes [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/).

The classes that derive from **InlineStory** are inline-level nodes that can contain
their own text (paragraphs and tables). For example, a **Comment** node contains text of a comment
and a **Footnote** contains text of a footnote.




**Inheritance:** [InlineStory](./) → [CompositeNode](../compositenode/) → [Node](../node/)

### Properties

| Name | Description |
| --- | --- |
| [child_nodes](../compositenode/child_nodes/) | Gets all immediate child nodes of this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [count](../compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [custom_node_id](../node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [first_child](../compositenode/first_child/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [first_paragraph](./first_paragraph/) | Gets the first paragraph in the story. |
| [font](./font/) | Provides access to the font formatting of the anchor character of this object. |
| [has_child_nodes](../compositenode/has_child_nodes/) | Returns true if this node has any child nodes.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [is_composite](../node/is_composite/) | Returns true if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [is_delete_revision](./is_delete_revision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [is_insert_revision](./is_insert_revision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [is_move_from_revision](./is_move_from_revision/) | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [is_move_to_revision](./is_move_to_revision/) | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [last_child](../compositenode/last_child/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [last_paragraph](./last_paragraph/) | Gets the last paragraph in the story. |
| [next_sibling](../node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [node_type](../node/node_type/) | Gets the type of this node.<br>(Inherited from [Node](../node/)) |
| [paragraphs](./paragraphs/) | Gets a collection of paragraphs that are immediate children of the story. |
| [parent_node](../node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [parent_paragraph](./parent_paragraph/) | Retrieves the parent [Paragraph](../paragraph/) of this node. |
| [previous_sibling](../node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a **Range** object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |
| [story_type](./story_type/) | Returns the type of the story. |
| [tables](./tables/) | Gets a collection of tables that are immediate children of the story. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](../node/accept/#documentvisitor) | Accepts a visitor.<br>(Inherited from [Node](../node/)) |
|[ append_child(new_child)](../compositenode/append_child/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ clone(is_clone_children)](../node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../node/)) |
|[ ensure_minimum()](./ensure_minimum/#default) | If the last child is not a paragraph, creates and appends one empty paragraph. |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ get_child(node_type, index, is_deep)](../compositenode/get_child/#nodetype_int_bool) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ get_child_nodes(node_type, is_deep)](../compositenode/get_child_nodes/#nodetype_bool) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ get_text()](../node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../node/)) |
|[ index_of(child)](../compositenode/index_of/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insert_after(new_child, ref_child)](../compositenode/insert_after/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insert_before(new_child, ref_child)](../compositenode/insert_before/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ next_pre_order(root_node)](../node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ node_type_to_string(node_type)](../node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../node/)) |
|[ prepend_child(new_child)](../compositenode/prepend_child/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ previous_pre_order(root_node)](../node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ remove()](../node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../node/)) |
|[ remove_all_children()](../compositenode/remove_all_children/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ remove_child(old_child)](../compositenode/remove_child/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ remove_smart_tags()](../compositenode/remove_smart_tags/#default) | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ select_nodes(xpath)](../compositenode/select_nodes/#str) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ select_single_node(xpath)](../compositenode/select_single_node/#str) | Selects the first Node that matches the XPath expression.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ to_string(save_format)](../node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ to_string(save_options)](../node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |

### Examples

Shows how to insert and customize footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Add text, and reference it with a footnote. This footnote will place a small superscript reference
# mark after the text that it references and create an entry below the main body text at the bottom of the page.
# This entry will contain the footnote's reference mark and the reference text,
# which we will pass to the document builder's "insert_footnote" method.
builder.write("Main body text.")
footnote = builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "Footnote text.")

# If this property is set to "True", then our footnote's reference mark
# will be its index among all the section's footnotes.
# This is the first footnote, so the reference mark will be "1".
self.assertTrue(footnote.is_auto)

# We can move the document builder inside the footnote to edit its reference text.
builder.move_to(footnote.first_paragraph)
builder.write(" More text added by a DocumentBuilder.")
builder.move_to_document_end()

self.assertEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.get_text().strip())

builder.write(" More main body text.")
footnote = builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "Footnote text.")

# We can set a custom reference mark which the footnote will use instead of its index number.
footnote.reference_mark = "RefMark"

self.assertFalse(footnote.is_auto)

# A bookmark with the "is_auto" flag set to True will still show its real index
# even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
builder.write(" More main body text.")
footnote = builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "Footnote text.")

self.assertTrue(footnote.is_auto)

doc.save(ARTIFACTS_DIR + "InlineStory.add_footnote.docx")
```

Shows how to add a comment to a paragraph.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write("Hello world!")

comment = aw.Comment(doc, "John Doe", "JD", date.today())
builder.current_paragraph.append_child(comment)
builder.move_to(comment.append_child(aw.Paragraph(doc)))
builder.write("Comment text.")

self.assertEqual(date.today(), comment.date_time.date())

# In Microsoft Word, we can right-click this comment in the document body to edit it, or reply to it.
doc.save(ARTIFACTS_DIR + "InlineStory.add_comment.docx")
```

### See Also

* module [aspose.words](../)
* class [CompositeNode](../compositenode/)

