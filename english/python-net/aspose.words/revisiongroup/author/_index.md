---
title: RevisionGroup.author property
linktitle: author property
articleTitle: author property
second_title: Aspose.Words for Python
description: "RevisionGroup.author property. Gets the author of this revision group."
type: docs
weight: 10
url: /python-net/aspose.words/revisiongroup/author/
---

## RevisionGroup.author property

Gets the author of this revision group.


```python
@property
def author(self) -> str:
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
* class [RevisionGroup](../)

