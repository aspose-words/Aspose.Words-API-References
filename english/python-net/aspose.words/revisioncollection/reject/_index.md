---
title: RevisionCollection.reject method
linktitle: reject method
articleTitle: reject method
second_title: Aspose.Words for Python
description: "RevisionCollection.reject method. Rejects revisions that match specified criteria."
type: docs
weight: 60
url: /python-net/aspose.words/revisioncollection/reject/
---

## reject(criteria) {#irevisioncriteria}

Rejects revisions that match specified criteria.


```python
def reject(self, criteria: aspose.words.IRevisionCriteria):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| criteria | [IRevisionCriteria](../../irevisioncriteria/) | The [IRevisionCriteria](../../irevisioncriteria/) implementation. |

### Returns

The count of rejected revisions.


### Examples

Shows how to accept or reject revision based on criteria.

```python
def test_revision_specified_criteria(self):
    doc = aw.Document()
    builder = aw.DocumentBuilder(doc=doc)
    builder.write('This does not count as a revision. ')
    # To register our edits as revisions, we need to declare an author, and then start tracking them.
    doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
    builder.write('This is insertion revision #1. ')
    doc.stop_track_revisions()
    doc.start_track_revisions(author='Jane Doe', date_time=datetime.datetime.now())
    builder.write('This is insertion revision #2. ')
    # Remove a run "This does not count as a revision.".
    doc.first_section.body.first_paragraph.runs[0].remove()
    doc.stop_track_revisions()
    self.assertEqual(3, doc.revisions.count)
    # We have two revisions from different authors, so we need to accept only one.
    doc.revisions.accept(self.RevisionCriteria('John Doe', aw.RevisionType.INSERTION))
    self.assertEqual(2, doc.revisions.count)
    # Reject revision with different author name and revision type.
    doc.revisions.reject(self.RevisionCriteria('Jane Doe', aw.RevisionType.DELETION))
    self.assertEqual(1, doc.revisions.count)
    doc.save(file_name=ARTIFACTS_DIR + 'Revision.RevisionSpecifiedCriteria.docx')

def test_track_revisions(self):
    from api_example_base import ApiExampleBase, ARTIFACTS_DIR
    import datetime
    import aspose.words as aw
    doc = aw.Document()
    builder = aw.DocumentBuilder(doc=doc)
    builder.write('Hello world! ')
    self.assertEqual(0, doc.revisions.count)
    self.assertFalse(doc.first_section.body.paragraphs[0].runs[0].is_insert_revision)
    doc.start_track_revisions(author='John Doe')
    builder.write('Hello again! ')
    self.assertEqual(1, doc.revisions.count)
    self.assertTrue(doc.first_section.body.paragraphs[0].runs[1].is_insert_revision)
    self.assertEqual('John Doe', doc.revisions[0].author)
    now = datetime.datetime.now(datetime.timezone.utc)
    self.assertTrue(abs((now - doc.revisions[0].date_time).total_seconds() * 1000) <= 10)
    doc.stop_track_revisions()
    builder.write('Hello again! ')
    self.assertEqual(1, doc.revisions.count)
    self.assertFalse(doc.first_section.body.paragraphs[0].runs[2].is_insert_revision)
    doc.start_track_revisions('John Doe', datetime.datetime.min.replace(tzinfo=None))
    builder.write('Hello again! ')
    self.assertEqual(2, doc.revisions.count)
    self.assertEqual('John Doe', doc.revisions[1].author)
    self.assertEqual(datetime.datetime.min.replace(tzinfo=None), doc.revisions[1].date_time)
    doc.save(file_name=ARTIFACTS_DIR + 'Revision.StartTrackRevisions.docx')
```

Shows how to accept or reject revision based on criteria.

```python
class RevisionCriteria(aw.IRevisionCriteria):

    def __init__(self, author_name, revision_type):
        self.author_name = author_name
        self.revision_type = revision_type

    def is_match(self, revision):
        return revision.author == self.author_name and revision.revision_type == self.revision_type
```

### See Also

* module [aspose.words](../../)
* class [RevisionCollection](../)

