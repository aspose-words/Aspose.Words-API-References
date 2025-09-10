---
title: BookmarkCollection indexer
linktitle: BookmarkCollection indexer
articleTitle: BookmarkCollection indexer
second_title: Aspose.Words for Python
description: "BookmarkCollection indexer. Returns a bookmark at the specified index."
type: docs
weight: 10
url: /python-net/aspose.words/bookmarkcollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Returns a bookmark at the specified index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. 
For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.




### See Also

* module [aspose.words](../../)
* class [BookmarkCollection](../)

