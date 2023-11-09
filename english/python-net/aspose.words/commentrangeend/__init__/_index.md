---
title: CommentRangeEnd constructor
linktitle: CommentRangeEnd constructor
articleTitle: CommentRangeEnd constructor
second_title: Aspose.Words for Python
description: "CommentRangeEnd constructor. Initializes a new instance of this class."
type: docs
weight: 10
url: /python-net/aspose.words/commentrangeend/__init__/
---

## CommentRangeEnd(doc, id) {#documentbase_int}

Initializes a new instance of this class.


```python
def __init__(self, doc: aspose.words.DocumentBase, id: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../documentbase/) | The owner document. |
| id | int | The comment identifier to which this object is linked. |

### Remarks

When [CommentRangeEnd](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parent_node](../../node/parent_node/) is ``None``.

To append a [CommentRangeEnd](../) to the document use InsertAfter or InsertBefore
on the paragraph where you want the comment inserted.




### See Also

* module [aspose.words](../../)
* class [CommentRangeEnd](../)

