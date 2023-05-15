﻿---
title: RevisionGroup class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents a group of sequential [Revision](../revision/) objects"
type: docs
weight: 940
url: /python-net/aspose.words/revisiongroup/
---

## RevisionGroup class

Represents a group of sequential [Revision](../revision/) objects.
To learn more, visit the [Track Changes in a Document](https://docs.aspose.com/words/python-net/track-changes-in-a-document/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [author](./author/) | Gets the author of this revision group. |
| [revision_type](./revision_type/) | Gets the type of revisions included in this group. |
| [text](./text/) | Returns inserted/deleted/moved text or description of format change. |

### Examples

Shows how to print info about a group of revisions in a document.

```python
doc = aw.Document(MY_DIR + "Revisions.docx")

self.assertEqual(7, doc.revisions.groups.count)

for group in doc.revisions.groups:
    print(f"Revision author: {group.author}; Revision type: {group.revision_type} \n\tRevision text: {group.text}")
```

### See Also

* module [aspose.words](../)

