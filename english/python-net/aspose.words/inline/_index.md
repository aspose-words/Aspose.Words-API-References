﻿---
title: Inline class
linktitle: Inline class
articleTitle: Inline class
second_title: Aspose.Words for Python
description: "aspose.words.Inline class. Base class for inline-level nodes that can have character formatting associated with them, but cannot have child nodes of their own"
type: docs
weight: 580
url: /python-net/aspose.words/inline/
---

## Inline class

Base class for inline-level nodes that can have character formatting associated with them, but cannot have child nodes of their own.
To learn more, visit the [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/python-net/logical-levels-of-nodes-in-a-document/) documentation article.




A class derived from [Inline](./) can be a child of [Paragraph](../paragraph/).




**Inheritance:** [Inline](./) → [Node](../node/)

### Properties

| Name | Description |
| --- | --- |
| [custom_node_id](../node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [font](./font/) | Provides access to the font formatting of this object. |
| [is_composite](../node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [is_delete_revision](./is_delete_revision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [is_format_revision](./is_format_revision/) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [is_insert_revision](./is_insert_revision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [is_move_from_revision](./is_move_from_revision/) | Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [is_move_to_revision](./is_move_to_revision/) | Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [next_sibling](../node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [node_type](../node/node_type/) | Gets the type of this node.<br>(Inherited from [Node](../node/)) |
| [parent_node](../node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [parent_paragraph](./parent_paragraph/) | Retrieves the parent [Paragraph](../paragraph/) of this node. |
| [previous_sibling](../node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](../node/accept/#documentvisitor) | Accepts a visitor.<br>(Inherited from [Node](../node/)) |
|[ clone(is_clone_children)](../node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../node/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#unknown) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../node/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ get_text()](../node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../node/)) |
|[ next_pre_order(root_node)](../node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ node_type_to_string(node_type)](../node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../node/)) |
|[ previous_pre_order(root_node)](../node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ remove()](../node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../node/)) |
|[ to_string(save_format)](../node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ to_string(save_options)](../node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |

### Examples

Shows how to determine the revision type of an inline node.

```python
doc = aw.Document(MY_DIR + "Revision runs.docx")

# When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
# is turned on in Microsoft Word, the changes we apply count as revisions.
# When editing a document using Aspose.Words, we can begin tracking revisions by
# invoking the document's "start_track_revisions" method and stop tracking by using the "stop_track_revisions" method.
# We can either accept revisions to assimilate them into the document
# or reject them to change the proposed change effectively.
self.assertEqual(6, doc.revisions.count)

# The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
run = doc.revisions[0].parent_node.as_run()

first_paragraph = run.parent_paragraph
runs = first_paragraph.runs

self.assertEqual(6, len(runs.to_array()))

# Below are five types of revisions that can flag an Inline node.
# 1 -  An "insert" revision:
# This revision occurs when we insert text while tracking changes.
self.assertTrue(runs[2].is_insert_revision)

# 2 -  A "format" revision:
# This revision occurs when we change the formatting of text while tracking changes.
self.assertTrue(runs[2].is_format_revision)

# 3 -  A "move from" revision:
# When we highlight text in Microsoft Word, and then drag it to a different place in the document
# while tracking changes, two revisions appear.
# The "move from" revision is a copy of the text originally before we moved it.
self.assertTrue(runs[4].is_move_from_revision)

# 4 -  A "move to" revision:
# The "move to" revision is the text that we moved in its new position in the document.
# "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
# Accepting a move revision deletes the "move from" revision and its text,
# and keeps the text from the "move to" revision.
# Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
self.assertTrue(runs[1].is_move_to_revision)

# 5 -  A "delete" revision:
# This revision occurs when we delete text while tracking changes. When we delete text like this,
# it will stay in the document as a revision until we either accept the revision,
# which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
self.assertTrue(runs[5].is_delete_revision)
```

### See Also

* module [aspose.words](../)
* class [Node](../node/)

