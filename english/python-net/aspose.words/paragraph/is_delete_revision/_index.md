---
title: is_delete_revision property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns true if this object was deleted in Microsoft Word while change tracking was enabled."
type: docs
weight: 40
url: /python-net/aspose.words/paragraph/is_delete_revision/
---

## Paragraph.is_delete_revision property

Returns true if this object was deleted in Microsoft Word while change tracking was enabled.


### Examples

Shows how to work with revision paragraphs.

```python
doc = aw.Document()
body = doc.first_section.body
para = body.first_paragraph

para.append_child(aw.Run(doc, "Paragraph 1. "))
body.append_paragraph("Paragraph 2. ")
body.append_paragraph("Paragraph 3. ")

# The above paragraphs are not revisions.
# Paragraphs that we add after starting revision tracking will register as "Insert" revisions.
doc.start_track_revisions("John Doe", datetime.now())

para = body.append_paragraph("Paragraph 4. ")

self.assertTrue(para.is_insert_revision)

# Paragraphs that we remove after starting revision tracking will register as "Delete" revisions.
paragraphs = body.paragraphs

self.assertEqual(4, paragraphs.count)

para = paragraphs[2]
para.remove()

# Such paragraphs will remain until we either accept or reject the delete revision.
# Accepting the revision will remove the paragraph for good,
# and rejecting the revision will leave it in the document as if we never deleted it.
self.assertEqual(4, paragraphs.count)
self.assertTrue(para.is_delete_revision)

# Accept the revision, and then verify that the paragraph is gone.
doc.accept_all_revisions()

self.assertEqual(3, paragraphs.count)
#self.assertEqual(para, "")
self.assertEqual(
    "Paragraph 1. \r" +
    "Paragraph 2. \r" +
    "Paragraph 4.", doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

