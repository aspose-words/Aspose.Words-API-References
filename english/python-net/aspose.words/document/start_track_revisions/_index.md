---
title: start_track_revisions method
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.Document.start_track_revisions method"
type: docs
weight: 680
url: /python-net/aspose.words/document/start_track_revisions/
---

## start_track_revisions(author, date_time) {#str_datetime}

Starts automatically marking all further changes you make to the document programmatically as revision changes.


```python
def start_track_revisions(self, author: str, date_time: datetime):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| author | str |  |
| date_time | datetime |  |

If you call this method and then make some changes to the document programmatically,
save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not
recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations
as well as when using [DocumentBuilder](../../documentbuilder/)

This method does not change the [Document.track_revisions](../track_revisions/) option and does not use its value
for the purposes of revision tracking.




## start_track_revisions(author) {#str}

Starts automatically marking all further changes you make to the document programmatically as revision changes.


```python
def start_track_revisions(self, author: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| author | str |  |

If you call this method and then make some changes to the document programmatically,
save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not
recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations
as well as when using [DocumentBuilder](../../documentbuilder/)

This method does not change the [Document.track_revisions](../track_revisions/) option and does not use its value
for the purposes of revision tracking.




## Examples

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

## See Also

* module [aspose.words](../../)
* class [Document](../)
* method [Document.stop_track_revisions()](../stop_track_revisions/#default)

