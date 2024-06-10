---
title: Range.revisions property
linktitle: revisions property
articleTitle: revisions property
second_title: Aspose.Words for Python
description: "Range.revisions property. Gets a collection of revisions (tracked changes) that exist in this range."
type: docs
weight: 40
url: /python-net/aspose.words/range/revisions/
---

## Range.revisions property

Gets a collection of revisions (tracked changes) that exist in this range.


```python
@property
def revisions(self) -> aspose.words.RevisionCollection:
    ...

```

### Remarks

The returned collection is a "live" collection, which means if you remove parts of a document that contain
revisions, the deleted revisions will automatically disappear from this collection.




### Examples

Shows how to work with revisions in range.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
paragraph = doc.first_section.body.first_paragraph
for revision in paragraph.range.revisions:
    if revision.revision_type == aw.RevisionType.DELETION:
        revision.accept()
# Reject the first section revisions.
doc.first_section.range.revisions.reject_all()
```

### See Also

* module [aspose.words](../../)
* class [Range](../)

