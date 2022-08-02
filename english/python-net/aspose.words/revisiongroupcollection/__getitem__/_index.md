---
title: RevisionGroupCollection indexer
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns a revision group at the specified index."
type: docs
weight: 10
url: /python-net/aspose.words/revisiongroupcollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Returns a revision group at the specified index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

Shows how to get a group of revisions in a document.

```python
doc = aw.Document(MY_DIR + "Revisions.docx")

revision_group = doc.revisions.groups[0]
```

### See Also

* module [aspose.words](../../)
* class [RevisionGroupCollection](../)

