---
title: revision_type property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets the type of revisions included in this group."
type: docs
weight: 20
url: /python-net/aspose.words/revisiongroup/revision_type/
---

## RevisionGroup.revision_type property

Gets the type of revisions included in this group.


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

