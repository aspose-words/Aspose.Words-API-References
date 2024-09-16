---
title: Comment class
linktitle: Comment class
articleTitle: Comment class
second_title: Aspose.Words for Python
description: "aspose.words.Comment class. Represents a container for text of a comment"
type: docs
weight: 170
url: /python-net/aspose.words/comment/
---

## Comment class

Represents a container for text of a comment.
To learn more, visit the [Working with Comments](https://docs.aspose.com/words/python-net/working-with-comments/) documentation article.




### Remarks

A comment is an annotation which is anchored to a region of text or to a position in text.
A comment can contain an arbitrary amount of block-level content.

If a [Comment](./) object occurs on its own, the comment is anchored to
the position of the [Comment](./) object.

To anchor a comment to a region of text three objects are required: [Comment](./),
[CommentRangeStart](../commentrangestart/) and [CommentRangeEnd](../commentrangeend/). All three objects need to share the same
[Comment.id](./id/) value.

[Comment](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).

[Comment](./) can contain [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.




**Inheritance:** [Comment](./) → [InlineStory](../inlinestory/) → [CompositeNode](../compositenode/) → [Node](../node/)

### Constructors
| Name | Description |
| --- | --- |
| [Comment(doc)](./__init__/#documentbase) | Initializes a new instance of the [Comment](./) class. |
| [Comment(doc, author, initial, date_time)](./__init__/#documentbase_str_str_datetime) | Initializes a new instance of the [Comment](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [ancestor](./ancestor/) | Returns the parent [Comment](./) object. Returns ``None`` for top-level comments. |
| [author](./author/) | Returns or sets the author name for a comment. |
| [count](../compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [custom_node_id](../node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [date_time](./date_time/) | Gets the date and time that the comment was made. |
| [date_time_utc](./date_time_utc/) | Gets the UTC date and time that the comment was made. |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [done](./done/) | Gets or sets flag indicating that the comment has been marked done. |
| [first_child](../compositenode/first_child/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [first_paragraph](../inlinestory/first_paragraph/) | Gets the first paragraph in the story.<br>(Inherited from [InlineStory](../inlinestory/)) |
| [font](../inlinestory/font/) | Provides access to the font formatting of the anchor character of this object.<br>(Inherited from [InlineStory](../inlinestory/)) |
| [has_child_nodes](../compositenode/has_child_nodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [id](./id/) | Gets or sets the comment identifier. |
| [initial](./initial/) | Returns or sets the initials of the user associated with a specific comment. |
| [is_composite](../node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [is_delete_revision](../inlinestory/is_delete_revision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled.<br>(Inherited from [InlineStory](../inlinestory/)) |
| [is_insert_revision](../inlinestory/is_insert_revision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled.<br>(Inherited from [InlineStory](../inlinestory/)) |
| [is_move_from_revision](../inlinestory/is_move_from_revision/) | Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [InlineStory](../inlinestory/)) |
| [is_move_to_revision](../inlinestory/is_move_to_revision/) | Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [InlineStory](../inlinestory/)) |
| [last_child](../compositenode/last_child/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [last_paragraph](../inlinestory/last_paragraph/) | Gets the last paragraph in the story.<br>(Inherited from [InlineStory](../inlinestory/)) |
| [next_sibling](../node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [node_type](./node_type/) | Returns [NodeType.COMMENT](../nodetype/#COMMENT). |
| [paragraphs](../inlinestory/paragraphs/) | Gets a collection of paragraphs that are immediate children of the story.<br>(Inherited from [InlineStory](../inlinestory/)) |
| [parent_id](./parent_id/) | Gets or sets the parent comment ID. A value of ``-1`` means the comment has no parent. |
| [parent_node](../node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [parent_paragraph](../inlinestory/parent_paragraph/) | Retrieves the parent [Paragraph](../paragraph/) of this node.<br>(Inherited from [InlineStory](../inlinestory/)) |
| [previous_sibling](../node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |
| [replies](./replies/) | Returns a collection of [Comment](./) objects that are immediate children of the specified comment. |
| [story_type](./story_type/) | Returns [StoryType.COMMENTS](../storytype/#COMMENTS). |
| [tables](../inlinestory/tables/) | Gets a collection of tables that are immediate children of the story.<br>(Inherited from [InlineStory](../inlinestory/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ accept_end(visitor)](./accept_end/#documentvisitor) | Accepts a visitor for visiting the end of the comment. |
|[ accept_start(visitor)](./accept_start/#documentvisitor) | Accepts a visitor for visiting the start of the comment. |
|[ add_reply(author, initial, date_time, text)](./add_reply/#str_str_datetime_str) | Adds a reply to this comment. |
|[ append_child(new_child)](../compositenode/append_child/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ clone(is_clone_children)](../node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../node/)) |
|[ ensure_minimum()](../inlinestory/ensure_minimum/#default) | If the last child is not a paragraph, creates and appends one empty paragraph.<br>(Inherited from [InlineStory](../inlinestory/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#object) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../node/)) |
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
|[ remove_all_replies()](./remove_all_replies/#default) | Removes all replies to this comment. |
|[ remove_child(old_child)](../compositenode/remove_child/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ remove_reply(reply)](./remove_reply/#comment) | Removes the specified reply to this comment. |
|[ remove_smart_tags()](../compositenode/remove_smart_tags/#default) | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ select_nodes(xpath)](../compositenode/select_nodes/#str) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ select_single_node(xpath)](../compositenode/select_single_node/#str) | Selects the first [Node](../node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ set_text(text)](./set_text/#str) | This is a convenience method that allows to easily set text of the comment. |
|[ to_string(save_format)](../node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ to_string(save_options)](../node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |

### Examples

Shows how to add a comment to a document, and then reply to it.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
comment = aw.Comment(doc=doc, author='John Doe', initial='J.D.', date_time=datetime.datetime.now())
comment.set_text('My comment.')
# Place the comment at a node in the document's body.
# This comment will show up at the location of its paragraph,
# outside the right-side margin of the page, and with a dotted line connecting it to its paragraph.
builder.current_paragraph.append_child(comment)
# Add a reply, which will show up under its parent comment.
comment.add_reply('Joe Bloggs', 'J.B.', datetime.datetime.now(), 'New reply')
# Comments and replies are both Comment nodes.
self.assertEqual(2, doc.get_child_nodes(aw.NodeType.COMMENT, True).count)
# Comments that do not reply to other comments are "top-level". They have no ancestor comments.
self.assertIsNone(comment.ancestor)
# Replies have an ancestor top-level comment.
self.assertEqual(comment, comment.replies[0].ancestor)
doc.save(file_name=ARTIFACTS_DIR + 'Comment.AddCommentWithReply.docx')
```

Shows how to add a comment to a paragraph.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('Hello world!')
comment = aw.Comment(doc, 'John Doe', 'JD', date.today())
builder.current_paragraph.append_child(comment)
builder.move_to(comment.append_child(aw.Paragraph(doc)))
builder.write('Comment text.')
self.assertEqual(date.today(), comment.date_time.date())
# In Microsoft Word, we can right-click this comment in the document body to edit it, or reply to it.
doc.save(ARTIFACTS_DIR + 'InlineStory.add_comment.docx')
```

### See Also

* module [aspose.words](../)
* class [InlineStory](../inlinestory/)
* class [CommentRangeStart](../commentrangestart/)
* class [CommentRangeEnd](../commentrangeend/)

