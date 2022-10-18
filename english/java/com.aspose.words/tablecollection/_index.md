---
title: TableCollection
second_title: Aspose.Words for Java API Reference
description: Provides typed access to a collection of  nodes.
type: docs
weight: 550
url: /java/com.aspose.words/tablecollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.NodeCollection](../../com.aspose.words/nodecollection)
```
public class TableCollection extends NodeCollection
```

Provides typed access to a collection of [Table](../../com.aspose.words/table) nodes.

To learn more, visit the **Working with Tables** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int-) | Retrieves a **Table** at the given index. |
| [toArray()](#toArray--) | Copies all tables from the collection to a new array of tables. |
### get(int index) {#get-int-}
```
public Node get(int index)
```


Retrieves a **Table** at the given index.

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

**Returns:**
[Node](../../com.aspose.words/node) - The corresponding [Table](../../com.aspose.words/table) value.
### toArray() {#toArray--}
```
public Node[] toArray()
```


Copies all tables from the collection to a new array of tables.

**Returns:**
com.aspose.words.Node[] - An array of tables.
