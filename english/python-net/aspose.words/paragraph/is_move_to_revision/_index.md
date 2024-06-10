---
title: Paragraph.is_move_to_revision property
linktitle: is_move_to_revision property
articleTitle: is_move_to_revision property
second_title: Aspose.Words for Python
description: "Paragraph.is_move_to_revision property. Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 140
url: /python-net/aspose.words/paragraph/is_move_to_revision/
---

## Paragraph.is_move_to_revision property

Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.



```python
@property
def is_move_to_revision(self) -> bool:
    ...

```

### Examples

Shows how to check whether a paragraph is a move revision.

```python
doc = aw.Document(MY_DIR + 'Revisions.docx')
# This document contains "Move" revisions, which appear when we highlight text with the cursor,
# and then drag it to move it to another location
# while tracking revisions in Microsoft Word via "Review" -> "Track changes".
self.assertEqual(6, len([r for r in doc.revisions if r.revision_type == aw.RevisionType.MOVING]))
paragraphs = doc.first_section.body.paragraphs
# Move revisions consist of pairs of "Move from", and "Move to" revisions.
# These revisions are potential changes to the document that we can either accept or reject.
# Before we accept/reject a move revision, the document
# must keep track of both the departure and arrival destinations of the text.
# The second and the fourth paragraph define one such revision, and thus both have the same contents.
self.assertEqual(paragraphs[1].get_text(), paragraphs[3].get_text())
# The "Move from" revision is the paragraph where we dragged the text from.
# If we accept the revision, this paragraph will disappear,
# and the other will remain and no longer be a revision.
self.assertTrue(paragraphs[1].is_move_from_revision)
# The "Move to" revision is the paragraph where we dragged the text to.
# If we reject the revision, this paragraph instead will disappear, and the other will remain.
self.assertTrue(paragraphs[3].is_move_to_revision)
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

