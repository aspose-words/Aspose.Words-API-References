---
title: Footnote class
linktitle: Footnote class
articleTitle: Footnote class
second_title: Aspose.Words for Python
description: "aspose.words.notes.Footnote class. Represents a container for text of a footnote or endnote"
type: docs
weight: 30
url: /python-net/aspose.words.notes/footnote/
---

## Footnote class

Represents a container for text of a footnote or endnote.
To learn more, visit the [Working with Footnote and Endnote](https://docs.aspose.com/words/python-net/working-with-footnote-and-endnote/) documentation article.




### Remarks

The [Footnote](./) class is used to represent both footnotes and endnotes in a Word document.

[Footnote](./) is an inline-level node and can only be a child of [Paragraph](../../aspose.words/paragraph/).

[Footnote](./) can contain [Paragraph](../../aspose.words/paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.




**Inheritance:** [Footnote](./) → [InlineStory](../../aspose.words/inlinestory/) → [CompositeNode](../../aspose.words/compositenode/) → [Node](../../aspose.words/node/)

### Constructors
| Name | Description |
| --- | --- |
| [Footnote(doc, footnote_type)](./__init__/#documentbase_footnotetype) | Initializes an instance of the [Footnote](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [actual_reference_mark](./actual_reference_mark/) | Gets the actual text of the reference mark displayed in the document for this footnote. |
| [count](../../aspose.words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [custom_node_id](../../aspose.words/node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [first_child](../../aspose.words/compositenode/first_child/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [first_paragraph](../../aspose.words/inlinestory/first_paragraph/) | Gets the first paragraph in the story.<br>(Inherited from [InlineStory](../../aspose.words/inlinestory/)) |
| [font](../../aspose.words/inlinestory/font/) | Provides access to the font formatting of the anchor character of this object.<br>(Inherited from [InlineStory](../../aspose.words/inlinestory/)) |
| [footnote_type](./footnote_type/) | Returns a value that specifies whether this is a footnote or endnote. |
| [has_child_nodes](../../aspose.words/compositenode/has_child_nodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [is_auto](./is_auto/) | Holds a value that specifies whether this is a auto-numbered footnote or  footnote with user defined custom reference mark. |
| [is_composite](../../aspose.words/node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [is_delete_revision](../../aspose.words/inlinestory/is_delete_revision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled.<br>(Inherited from [InlineStory](../../aspose.words/inlinestory/)) |
| [is_insert_revision](../../aspose.words/inlinestory/is_insert_revision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled.<br>(Inherited from [InlineStory](../../aspose.words/inlinestory/)) |
| [is_move_from_revision](../../aspose.words/inlinestory/is_move_from_revision/) | Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [InlineStory](../../aspose.words/inlinestory/)) |
| [is_move_to_revision](../../aspose.words/inlinestory/is_move_to_revision/) | Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [InlineStory](../../aspose.words/inlinestory/)) |
| [last_child](../../aspose.words/compositenode/last_child/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [last_paragraph](../../aspose.words/inlinestory/last_paragraph/) | Gets the last paragraph in the story.<br>(Inherited from [InlineStory](../../aspose.words/inlinestory/)) |
| [next_sibling](../../aspose.words/node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [node_type](./node_type/) | Returns [NodeType.FOOTNOTE](../../aspose.words/nodetype/#FOOTNOTE). |
| [paragraphs](../../aspose.words/inlinestory/paragraphs/) | Gets a collection of paragraphs that are immediate children of the story.<br>(Inherited from [InlineStory](../../aspose.words/inlinestory/)) |
| [parent_node](../../aspose.words/node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [parent_paragraph](../../aspose.words/inlinestory/parent_paragraph/) | Retrieves the parent [Paragraph](../../aspose.words/paragraph/) of this node.<br>(Inherited from [InlineStory](../../aspose.words/inlinestory/)) |
| [previous_sibling](../../aspose.words/node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [reference_mark](./reference_mark/) | Gets/sets custom reference mark to be used for this footnote. Default value is **empty string** (), meaning auto-numbered footnotes are used. |
| [story_type](./story_type/) | Returns [StoryType.FOOTNOTES](../../aspose.words/storytype/#FOOTNOTES) or [StoryType.ENDNOTES](../../aspose.words/storytype/#ENDNOTES). |
| [tables](../../aspose.words/inlinestory/tables/) | Gets a collection of tables that are immediate children of the story.<br>(Inherited from [InlineStory](../../aspose.words/inlinestory/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ accept_end(visitor)](./accept_end/#documentvisitor) | Accepts a visitor for visiting the end of the footnote. |
|[ accept_start(visitor)](./accept_start/#documentvisitor) | Accepts a visitor for visiting the start of the footnote. |
|[ append_child(new_child)](../../aspose.words/compositenode/append_child/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ clone(is_clone_children)](../../aspose.words/node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ ensure_minimum()](../../aspose.words/inlinestory/ensure_minimum/#default) | If the last child is not a paragraph, creates and appends one empty paragraph.<br>(Inherited from [InlineStory](../../aspose.words/inlinestory/)) |
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

Shows how to insert and customize footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Add text, and reference it with a footnote. This footnote will place a small superscript reference
# mark after the text that it references and create an entry below the main body text at the bottom of the page.
# This entry will contain the footnote's reference mark and the reference text,
# which we will pass to the document builder's "insert_footnote" method.
builder.write('Main body text.')
footnote = builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, 'Footnote text.')
# If this property is set to "True", then our footnote's reference mark
# will be its index among all the section's footnotes.
# This is the first footnote, so the reference mark will be "1".
self.assertTrue(footnote.is_auto)
# We can move the document builder inside the footnote to edit its reference text.
builder.move_to(footnote.first_paragraph)
builder.write(' More text added by a DocumentBuilder.')
builder.move_to_document_end()
self.assertEqual('\x02 Footnote text. More text added by a DocumentBuilder.', footnote.get_text().strip())
builder.write(' More main body text.')
footnote = builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, 'Footnote text.')
# We can set a custom reference mark which the footnote will use instead of its index number.
footnote.reference_mark = 'RefMark'
self.assertFalse(footnote.is_auto)
# A bookmark with the "is_auto" flag set to True will still show its real index
# even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
builder.write(' More main body text.')
footnote = builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, 'Footnote text.')
self.assertTrue(footnote.is_auto)
doc.save(ARTIFACTS_DIR + 'InlineStory.add_footnote.docx')
```

### See Also

* module [aspose.words.notes](../)
* class [InlineStory](../../aspose.words/inlinestory/)
* property [Footnote.footnote_type](./footnote_type/)
* method [DocumentBuilder.insert_footnote()](../../aspose.words/documentbuilder/insert_footnote/#footnotetype_str)
* class [FootnoteOptions](../footnoteoptions/)
* class [EndnoteOptions](../endnoteoptions/)

