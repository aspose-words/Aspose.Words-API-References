---
title: Document.stop_track_revisions method
linktitle: stop_track_revisions method
articleTitle: stop_track_revisions method
second_title: Aspose.Words for Python
description: "Document.stop_track_revisions method. Stops automatic marking of document changes as revisions."
type: docs
weight: 730
url: /python-net/aspose.words/document/stop_track_revisions/
---

## stop_track_revisions() {#default}

Stops automatic marking of document changes as revisions.


```python
def stop_track_revisions(self):
    ...
```

### Examples

Shows how to track revisions while editing a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Editing a document usually does not count as a revision until we begin tracking them.
builder.write("Hello world! ")

self.assertEqual(0, doc.revisions.count)
self.assertFalse(doc.first_section.body.paragraphs[0].runs[0].is_insert_revision)

doc.start_track_revisions("John Doe")

builder.write("Hello again! ")

self.assertEqual(1, doc.revisions.count)
self.assertTrue(doc.first_section.body.paragraphs[0].runs[1].is_insert_revision)
self.assertEqual("John Doe", doc.revisions[0].author)
self.assertAlmostEqual(doc.revisions[0].date_time, datetime.now(tz=timezone.utc), delta=timedelta(seconds=1))

# Stop tracking revisions to not count any future edits as revisions.
doc.stop_track_revisions()
builder.write("Hello again! ")

self.assertEqual(1, doc.revisions.count)
self.assertFalse(doc.first_section.body.paragraphs[0].runs[2].is_insert_revision)

# Creating revisions gives them a date and time of the operation.
# We can disable this by passing "datetime.min" when we start tracking revisions.
doc.start_track_revisions("John Doe", datetime.min)
builder.write("Hello again! ")

self.assertEqual(2, doc.revisions.count)
self.assertEqual("John Doe", doc.revisions[1].author)
self.assertEqual(datetime.min, doc.revisions[1].date_time)

# We can accept/reject these revisions programmatically
# by calling methods such as "Document.accept_all_revisions", or each revision's "accept" method.
# In Microsoft Word, we can process them manually via "Review" -> "Changes".
doc.save(ARTIFACTS_DIR + "Document.track_revisions.docx")
```

### See Also

* module [aspose.words](../../)
* class [Document](../)
* method [Document.start_track_revisions()](../start_track_revisions/#str_datetime)

