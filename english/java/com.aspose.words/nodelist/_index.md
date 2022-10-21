---
title: NodeList
second_title: Aspose.Words for Java API Reference
description: Represents a collection of nodes matching an XPath query executed using the  method.
type: docs
weight: 406
url: /java/com.aspose.words/nodelist/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class NodeList implements Iterable
```

Represents a collection of nodes matching an XPath query executed using the [CompositeNode.selectNodes(java.lang.String)](../../com.aspose.words/compositenode\#selectNodes-java.lang.String-) method.

To learn more, visit the **Aspose.Words Document Object Model (DOM)** documentation article.

**NodeList** is returned by [CompositeNode.selectNodes(java.lang.String)](../../com.aspose.words/compositenode\#selectNodes-java.lang.String-) and contains a collection of nodes matching the XPath query.

**NodeList** supports indexed access and iteration.

Treat the **NodeList** collection as a "snapshot" collection. **NodeList** starts as a "live" collection because the nodes are not actually retrieved when the XPath query is run. The nodes are only retrieved upon access and at this time the node and all nodes that precede it are cached forming a "snapshot" collection.
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int-) | Retrieves a node at the given index. |
| [getCount()](#getCount--) | Gets the number of nodes in the list. |
| [toArray()](#toArray--) | Copies all nodes from the collection to a new array of nodes. |
| [iterator()](#iterator--) | Provides a simple "foreach" style iteration over the collection of nodes. |
### get(int index) {#get-int-}
```
public Node get(int index)
```


Retrieves a node at the given index.

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the list of nodes. |

**Returns:**
[Node](../../com.aspose.words/node) - The corresponding [Node](../../com.aspose.words/node) value.
### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of nodes in the list.

**Returns:**
int - The number of nodes in the list.
### toArray() {#toArray--}
```
public Node[] toArray()
```


Copies all nodes from the collection to a new array of nodes.

You should not be adding/removing nodes while iterating over a collection of nodes because it invalidates the iterator and requires refreshes for live collections.

To be able to add/remove nodes during iteration, use this method to copy nodes into a fixed-size array and then iterate over the array.

**Returns:**
com.aspose.words.Node[] - An array of nodes.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Provides a simple "foreach" style iteration over the collection of nodes.

**Returns:**
java.util.Iterator - An Iterator.
