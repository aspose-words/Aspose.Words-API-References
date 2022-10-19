---
title: NodeCollection
second_title: Aspose.Words for Java API Reference
description: Represents a collection of nodes of a specific type.
type: docs
weight: 404
url: /java/com.aspose.words/nodecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class NodeCollection implements Iterable
```

Represents a collection of nodes of a specific type.

To learn more, visit the **Aspose.Words Document Object Model (DOM)** documentation article.

**NodeCollection** does not own the nodes it contains, rather, is just a selection of nodes of the specified type, but the nodes are stored in the tree under their respective parent nodes.

**NodeCollection** supports indexed access, iteration and provides add and remove methods.

The **NodeCollection** collection is "live", i.e. changes to the children of the node object that it was created from are immediately reflected in the nodes returned by the **NodeCollection** properties and methods.

**NodeCollection** is returned by **M:Aspose.Words.CompositeNode.GetChildNodes(Aspose.Words.NodeType,System.Boolean)** and also serves as a base class for typed node collections such as [SectionCollection](../../com.aspose.words/sectioncollection), [ParagraphCollection](../../com.aspose.words/paragraphcollection) etc.

**NodeCollection** can be "flat" and contain only immediate children of the node it was created from, or it can be "deep" and contain all descendant children.
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int-) | Retrieves a node at the given index. |
| [add(Node node)](#add-com.aspose.words.Node-) | Adds a node to the end of the collection. |
| [insert(int index, Node node)](#insert-int-com.aspose.words.Node-) | Inserts a node into the collection at the specified index. |
| [remove(Node node)](#remove-com.aspose.words.Node-) | Removes the node from the collection and from the document. |
| [removeAt(int index)](#removeAt-int-) | Removes the node at the specified index from the collection and from the document. |
| [clear()](#clear--) | Removes all nodes from this collection and from the document. |
| [contains(Node node)](#contains-com.aspose.words.Node-) | Determines whether a node is in the collection. |
| [indexOf(Node node)](#indexOf-com.aspose.words.Node-) | Returns the zero-based index of the specified node. |
| [toArray()](#toArray--) | Copies all nodes from the collection to a new array of nodes. |
| [iterator()](#iterator--) | Provides a simple "foreach" style iteration over the collection of nodes. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getCount()](#getCount--) | Gets the number of nodes in the collection. |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getContainer()](#getContainer--) |  |
### get(int index) {#get-int-}
```
public Node get(int index)
```


Retrieves a node at the given index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection of nodes.

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference. |

**Returns:**
[Node](../../com.aspose.words/node) - The corresponding [Node](../../com.aspose.words/node) value.
### add(Node node) {#add-com.aspose.words.Node-}
```
public void add(Node node)
```


Adds a node to the end of the collection.

The node is inserted as a child into the node object from which the collection was created.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) | The node to be added to the end of the collection. |

### insert(int index, Node node) {#insert-int-com.aspose.words.Node-}
```
public void insert(int index, Node node)
```


Inserts a node into the collection at the specified index.

The node is inserted as a child into the node object from which the collection was created.

If the index is equal to or greater than Count, the node is added at the end of the collection.

If the index is negative and its absolute value is greater than Count, the node is added at the end of the collection.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the node. Negative indexes are allowed and indicate access from the back of the list. For example -1 means the last node, -2 means the second before last and so on. |
| node | [Node](../../com.aspose.words/node) | The node to insert. |

### remove(Node node) {#remove-com.aspose.words.Node-}
```
public void remove(Node node)
```


Removes the node from the collection and from the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) | The node to remove. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Removes the node at the specified index from the collection and from the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the node. Negative indexes are allowed and indicate access from the back of the list. For example -1 means the last node, -2 means the second before last and so on. |

### clear() {#clear--}
```
public void clear()
```


Removes all nodes from this collection and from the document.

### contains(Node node) {#contains-com.aspose.words.Node-}
```
public boolean contains(Node node)
```


Determines whether a node is in the collection.

This method performs a linear search; therefore, the average execution time is proportional to Count.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) | The node to locate. |

**Returns:**
boolean - True if item is found in the collection; otherwise, false.
### indexOf(Node node) {#indexOf-com.aspose.words.Node-}
```
public int indexOf(Node node)
```


Returns the zero-based index of the specified node.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) | The node to locate. |

**Returns:**
int - The zero-based index of the node within the collection, if found; otherwise, -1.

This method performs a linear search; therefore, the average execution time is proportional to Count.
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
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node-}
```
public Node getNextMatchingNode(Node curNode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node) |  |

**Returns:**
[Node](../../com.aspose.words/node)
### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of nodes in the collection.

**Returns:**
int - The number of nodes in the collection.
### getCurrentNode() {#getCurrentNode--}
```
public Node getCurrentNode()
```




**Returns:**
[Node](../../com.aspose.words/node)
### getContainer() {#getContainer--}
```
public CompositeNode getContainer()
```




**Returns:**
[CompositeNode](../../com.aspose.words/compositenode)