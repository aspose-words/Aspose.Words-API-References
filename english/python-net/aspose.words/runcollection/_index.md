---
title: RunCollection class
linktitle: RunCollection class
articleTitle: RunCollection class
second_title: Aspose.Words for Python
description: "aspose.words.RunCollection class. Provides typed access to a collection of [Run](../run/) nodes"
type: docs
weight: 1050
url: /python-net/aspose.words/runcollection/
---

## RunCollection class

Provides typed access to a collection of [Run](../run/) nodes.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/python-net/programming-with-documents/) documentation article.




**Inheritance:** [RunCollection](./) → [NodeCollection](../nodecollection/)

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Retrieves a [Run](../run/) at the given index. |

### Properties

| Name | Description |
| --- | --- |
| [count](../nodecollection/count/) | Gets the number of nodes in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |

### Methods

| Name | Description |
| --- | --- |
|[ add(node)](../nodecollection/add/#node) | Adds a node to the end of the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ clear()](../nodecollection/clear/#default) | Removes all nodes from this collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ contains(node)](../nodecollection/contains/#node) | Determines whether a node is in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ index_of(node)](../nodecollection/index_of/#node) | Returns the zero-based index of the specified node.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ insert(index, node)](../nodecollection/insert/#int_node) | Inserts a node into the collection at the specified index.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ remove(node)](../nodecollection/remove/#node) | Removes the node from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ remove_at(index)](../nodecollection/remove_at/#int) | Removes the node at the specified index from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ to_array()](./to_array/#default) | Copies all runs from the collection to a new array of runs. |

### Examples

Shows how to determine the revision type of an inline node.

```python
doc = aw.Document(file_name=MY_DIR + 'Revision runs.docx')
# When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
# is turned on in Microsoft Word, the changes we apply count as revisions.
# When editing a document using Aspose.Words, we can begin tracking revisions by
# invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
# We can either accept revisions to assimilate them into the document
# or reject them to change the proposed change effectively.
self.assertEqual(6, doc.revisions.count)
# The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
run = doc.revisions[0].parent_node.as_run()
first_paragraph = run.parent_paragraph
runs = first_paragraph.runs
self.assertEqual(6, len(list(runs)))
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
* class [NodeCollection](../nodecollection/)

