---
title: RevisionGroup.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "RevisionGroup.text property. Returns inserted/deleted/moved text or description of format change."
type: docs
weight: 30
url: /python-net/aspose.words/revisiongroup/text/
---

## RevisionGroup.text property

Returns inserted/deleted/moved text or description of format change.


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

