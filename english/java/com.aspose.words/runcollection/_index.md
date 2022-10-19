---
title: RunCollection
second_title: Aspose.Words for Java API Reference
description: Provides typed access to a collection of  nodes.
type: docs
weight: 498
url: /java/com.aspose.words/runcollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.NodeCollection](../../com.aspose.words/nodecollection)
```
public class RunCollection extends NodeCollection
```

Provides typed access to a collection of [Run](../../com.aspose.words/run) nodes.

To learn more, visit the **Programming with Documents** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int-) | Retrieves a **Run** at the given index. |
| [toArray()](#toArray--) | Copies all runs from the collection to a new array of runs. |
### get(int index) {#get-int-}
```
public Node get(int index)
```


Retrieves a **Run** at the given index.

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

**Returns:**
[Node](../../com.aspose.words/node) - The corresponding [Run](../../com.aspose.words/run) value.
### toArray() {#toArray--}
```
public Node[] toArray()
```


Copies all runs from the collection to a new array of runs.

**Returns:**
com.aspose.words.Node[] - An array of runs.
