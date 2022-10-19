---
title: BuildingBlockCollection
second_title: Aspose.Words for Java API Reference
description: A collection of  objects in the document.
type: docs
weight: 43
url: /java/com.aspose.words/buildingblockcollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.NodeCollection](../../com.aspose.words/nodecollection)
```
public class BuildingBlockCollection extends NodeCollection
```

A collection of [BuildingBlock](../../com.aspose.words/buildingblock) objects in the document.

To learn more, visit the **Aspose.Words Document Object Model (DOM)** documentation article.

You do not create instances of this class directly. To access a collection of building blocks use the [GlossaryDocument.getBuildingBlocks()](../../com.aspose.words/glossarydocument\#getBuildingBlocks--) property.
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int-) | Retrieves a building block at the given index. |
| [toArray()](#toArray--) | Copies all building blocks from the collection to a new array of building blocks. |
### get(int index) {#get-int-}
```
public Node get(int index)
```


Retrieves a building block at the given index.

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the list of building blocks. |

**Returns:**
[Node](../../com.aspose.words/node) - The corresponding [BuildingBlock](../../com.aspose.words/buildingblock) value.
### toArray() {#toArray--}
```
public Node[] toArray()
```


Copies all building blocks from the collection to a new array of building blocks.

**Returns:**
com.aspose.words.Node[] - An array of building blocks.
