---
title: CommentCollection
second_title: Aspose.Words for Java API Reference
description: Provides typed access to a collection of  nodes.
type: docs
weight: 77
url: /java/com.aspose.words/commentcollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.NodeCollection](../../com.aspose.words/nodecollection)
```
public class CommentCollection extends NodeCollection
```

Provides typed access to a collection of [Comment](../../com.aspose.words/comment) nodes.

To learn more, visit the **Working with Comments** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int-) | Retrieves a **Comment** at the given index. |
### get(int index) {#get-int-}
```
public Comment get(int index)
```


Retrieves a **Comment** at the given index.

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

**Returns:**
[Comment](../../com.aspose.words/comment) - The corresponding [Comment](../../com.aspose.words/comment) value.
