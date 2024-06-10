---
title: InlineStory.is_move_from_revision property
linktitle: is_move_from_revision property
articleTitle: is_move_from_revision property
second_title: Aspose.Words for Python
description: "InlineStory.is_move_from_revision property. Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 50
url: /python-net/aspose.words/inlinestory/is_move_from_revision/
---

## InlineStory.is_move_from_revision property

Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.



```python
@property
def is_move_from_revision(self) -> bool:
    ...

```

### Examples

Shows how to view revision-related properties of InlineStory nodes.

```python
doc = aw.Document(MY_DIR + 'Revision footnotes.docx')
# When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
# is turned on in Microsoft Word, the changes we apply count as revisions.
# When editing a document using Aspose.Words, we can begin tracking revisions by
# invoking the document's "start_track_revisions" method and stop tracking by using the "stop_track_revisions" method.
# We can either accept revisions to assimilate them into the document
# or reject them to undo and discard the proposed change.
self.assertTrue(doc.has_revisions)
footnotes = [node.as_footnote() for node in doc.get_child_nodes(aw.NodeType.FOOTNOTE, True)]
self.assertEqual(5, len(footnotes))
# Below are five types of revisions that can flag an InlineStory node.
# 1 -  An "insert" revision:
# This revision occurs when we insert text while tracking changes.
self.assertTrue(footnotes[2].is_insert_revision)
# 2 -  A "move from" revision:
# When we highlight text in Microsoft Word, and then drag it to a different place in the document
# while tracking changes, two revisions appear.
# The "move from" revision is a copy of the text originally before we moved it.
self.assertTrue(footnotes[4].is_move_from_revision)
# 3 -  A "move to" revision:
# The "move to" revision is the text that we moved in its new position in the document.
# "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
# Accepting a move revision deletes the "move from" revision and its text,
# and keeps the text from the "move to" revision.
# Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
self.assertTrue(footnotes[1].is_move_to_revision)
# 4 -  A "delete" revision:
# This revision occurs when we delete text while tracking changes. When we delete text like this,
# it will stay in the document as a revision until we either accept the revision,
# which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
self.assertTrue(footnotes[3].is_delete_revision)
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

