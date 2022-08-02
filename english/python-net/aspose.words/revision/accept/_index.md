---
title: accept method
second_title: Aspose.Words for Python via .NET API Reference
description: "Accepts this revision."
type: docs
weight: 70
url: /python-net/aspose.words/revision/accept/
---

## accept() {#default}

Accepts this revision.


```python
def accept(self):
    ...
```

### Examples

Shows how to work with revisions in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Normal editing of the document does not count as a revision.
builder.write("This does not count as a revision. ")

self.assertFalse(doc.has_revisions)

# To register our edits as revisions, we need to declare an author, and then start tracking them.
doc.start_track_revisions("John Doe", datetime.now())

builder.write("This is revision #1. ")

self.assertTrue(doc.has_revisions)
self.assertEqual(1, doc.revisions.count)

# This flag corresponds to the "Review" -> "Tracking" -> "Track Changes" option in Microsoft Word.
# The "start_track_revisions" method does not affect its value,
# and the document is tracking revisions programmatically despite it having a value of "False".
# If we open this document using Microsoft Word, it will not be tracking revisions.
self.assertFalse(doc.track_revisions)

# We have added text using the document builder, so the first revision is an insertion-type revision.
revision = doc.revisions[0]
self.assertEqual("John Doe", revision.author)
self.assertEqual("This is revision #1. ", revision.parent_node.get_text())
self.assertEqual(aw.RevisionType.INSERTION, revision.revision_type)
self.assertEqual(revision.date_time.date(), date.today())
self.assertEqual(doc.revisions.groups[0], revision.group)

# Remove a run to create a deletion-type revision.
doc.first_section.body.first_paragraph.runs[0].remove()

# Adding a new revision places it at the beginning of the revision collection.
self.assertEqual(aw.RevisionType.DELETION, doc.revisions[0].revision_type)
self.assertEqual(2, doc.revisions.count)

# Insert revisions show up in the document body even before we accept/reject the revision.
# Rejecting the revision will remove its nodes from the body. Conversely, nodes that make up delete revisions
# also linger in the document until we accept the revision.
self.assertEqual("This does not count as a revision. This is revision #1.", doc.get_text().strip())

# Accepting the delete revision will remove its parent node from the paragraph text
# and then remove the collection's revision itself.
doc.revisions[0].accept()

self.assertEqual(1, doc.revisions.count)
self.assertEqual("This is revision #1.", doc.get_text().strip())

builder.writeln("")
builder.write("This is revision #2.")

# Now move the node to create a moving revision type.
node = doc.first_section.body.paragraphs[1]
end_node = doc.first_section.body.paragraphs[1].next_sibling
reference_node = doc.first_section.body.paragraphs[0]

while node != end_node:
    next_node = node.next_sibling
    doc.first_section.body.insert_before(node, reference_node)
    node = next_node

self.assertEqual(aw.RevisionType.MOVING, doc.revisions[0].revision_type)
self.assertEqual(8, doc.revisions.count)
self.assertEqual("This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc.get_text().strip())

# The moving revision is now at index 1. Reject the revision to discard its contents.
doc.revisions[1].reject()

self.assertEqual(6, doc.revisions.count)
self.assertEqual("This is revision #1. \rThis is revision #2.", doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Revision](../)

