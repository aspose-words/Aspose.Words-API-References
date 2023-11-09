---
title: RevisionGroupCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "RevisionGroupCollection.count property. Returns the number of revision groups in the collection."
type: docs
weight: 20
url: /python-net/aspose.words/revisiongroupcollection/count/
---

## RevisionGroupCollection.count property

Returns the number of revision groups in the collection.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to print info about a group of revisions in a document.

```python
doc = aw.Document(MY_DIR + "Revisions.docx")

self.assertEqual(7, doc.revisions.groups.count)

for group in doc.revisions.groups:
    print(f"Revision author: {group.author}; Revision type: {group.revision_type} \n\tRevision text: {group.text}")
```

### See Also

* module [aspose.words](../../)
* class [RevisionGroupCollection](../)

