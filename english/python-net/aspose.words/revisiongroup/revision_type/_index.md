---
title: RevisionGroup.revision_type property
linktitle: revision_type property
articleTitle: revision_type property
second_title: Aspose.Words for Python
description: "RevisionGroup.revision_type property. Gets the type of revisions included in this group."
type: docs
weight: 20
url: /python-net/aspose.words/revisiongroup/revision_type/
---

## RevisionGroup.revision_type property

Gets the type of revisions included in this group.


```python
@property
def revision_type(self) -> aspose.words.RevisionType:
    ...

```

### Examples

Shows how to print info about a group of revisions in a document.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
self.assertEqual(7, doc.revisions.groups.count)
for group in doc.revisions.groups:
    print(f'Revision author: {group.author}; Revision type: {group.revision_type} \n\tRevision text: {group.text}')
```

### See Also

* module [aspose.words](../../)
* class [RevisionGroup](../)

