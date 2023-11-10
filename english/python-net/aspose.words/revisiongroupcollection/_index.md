---
title: RevisionGroupCollection class
linktitle: RevisionGroupCollection class
articleTitle: RevisionGroupCollection class
second_title: Aspose.Words for Python
description: "aspose.words.RevisionGroupCollection class. A collection of [RevisionGroup](../revisiongroup/) objects that represent revision groups in the document"
type: docs
weight: 980
url: /python-net/aspose.words/revisiongroupcollection/
---

## RevisionGroupCollection class

A collection of [RevisionGroup](../revisiongroup/) objects that represent revision groups in the document.
To learn more, visit the [Track Changes in a Document](https://docs.aspose.com/words/python-net/track-changes-in-a-document/) documentation article.




### Remarks

You do not create instances of this class directly. Use the [RevisionCollection.groups](../revisioncollection/groups/)
property to get revision groups present in a document.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Returns a revision group at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of revision groups in the collection. |

### Examples

Shows how to print info about a group of revisions in a document.

```python
doc = aw.Document(MY_DIR + "Revisions.docx")

self.assertEqual(7, doc.revisions.groups.count)

for group in doc.revisions.groups:
    print(f"Revision author: {group.author}; Revision type: {group.revision_type} \n\tRevision text: {group.text}")
```

Shows how to get a group of revisions in a document.

```python
doc = aw.Document(MY_DIR + "Revisions.docx")

revision_group = doc.revisions.groups[0]
```

### See Also

* module [aspose.words](../)

