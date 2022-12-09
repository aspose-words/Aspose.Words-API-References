---
title: NodeCollection
second_title: Aspose.Words for Java API Reference
description: Represents a collection of nodes of a specific type.
type: docs
weight: 407
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

To learn more, visit the [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_] documentation article.

[NodeCollection](../../com.aspose.words/nodecollection) does not own the nodes it contains, rather, is just a selection of nodes of the specified type, but the nodes are stored in the tree under their respective parent nodes.

[NodeCollection](../../com.aspose.words/nodecollection) supports indexed access, iteration and provides add and remove methods.

The [NodeCollection](../../com.aspose.words/nodecollection) collection is "live", i.e. changes to the children of the node object that it was created from are immediately reflected in the nodes returned by the [NodeCollection](../../com.aspose.words/nodecollection) properties and methods.

[NodeCollection](../../com.aspose.words/nodecollection) is returned by **M:Aspose.Words.CompositeNode.GetChildNodes(Aspose.Words.NodeType,System.Boolean)** and also serves as a base class for typed node collections such as [SectionCollection](../../com.aspose.words/sectioncollection), [ParagraphCollection](../../com.aspose.words/paragraphcollection) etc.

[NodeCollection](../../com.aspose.words/nodecollection) can be "flat" and contain only immediate children of the node it was created from, or it can be "deep" and contain all descendant children.


[Aspose.Words Document Object Model _DOM_]: https://docs.aspose.com/words/java/aspose-words-document-object-model/
## Methods

| Method | Description |
| --- | --- |
| [add(Node node)](#add-com.aspose.words.Node) | Adds a node to the end of the collection. |
| [clear()](#clear) | Removes all nodes from this collection and from the document. |
| [contains(Node node)](#contains-com.aspose.words.Node) | Determines whether a node is in the collection. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(int index)](#get-int) | Retrieves a node at the given index. |
| [getClass()](#getClass) |  |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Gets the number of nodes in the collection. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [hashCode()](#hashCode) |  |
| [indexOf(Node node)](#indexOf-com.aspose.words.Node) | Returns the zero-based index of the specified node. |
| [insert(int index, Node node)](#insert-int-com.aspose.words.Node) | Inserts a node into the collection at the specified index. |
| [iterator()](#iterator) | Provides a simple "foreach" style iteration over the collection of nodes. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove(Node node)](#remove-com.aspose.words.Node) | Removes the node from the collection and from the document. |
| [removeAt(int index)](#removeAt-int) | Removes the node at the specified index from the collection and from the document. |
| [toArray()](#toArray) | Copies all nodes from the collection to a new array of nodes. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### add(Node node) {#add-com.aspose.words.Node}
```
public void add(Node node)
```


Adds a node to the end of the collection.

The node is inserted as a child into the node object from which the collection was created.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) | The node to be added to the end of the collection. |

### clear() {#clear}
```
public void clear()
```


Removes all nodes from this collection and from the document.

### contains(Node node) {#contains-com.aspose.words.Node}
```
public boolean contains(Node node)
```


Determines whether a node is in the collection.

This method performs a linear search; therefore, the average execution time is proportional to [getCount()](../../com.aspose.words/nodecollection\#getCount).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) | The node to locate. |

**Returns:**
boolean - \{ true  if item is found in the collection; otherwise,  false .
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### get(int index) {#get-int}
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getContainer() {#getContainer}
```
public CompositeNode getContainer()
```




**Returns:**
[CompositeNode](../../com.aspose.words/compositenode)
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of nodes in the collection.

**Returns:**
int - The number of nodes in the collection.
### getCurrentNode() {#getCurrentNode}
```
public Node getCurrentNode()
```




**Returns:**
[Node](../../com.aspose.words/node)
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node}
```
public Node getNextMatchingNode(Node curNode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node) |  |

**Returns:**
[Node](../../com.aspose.words/node)
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### indexOf(Node node) {#indexOf-com.aspose.words.Node}
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

This method performs a linear search; therefore, the average execution time is proportional to [getCount()](../../com.aspose.words/nodecollection\#getCount).
### insert(int index, Node node) {#insert-int-com.aspose.words.Node}
```
public void insert(int index, Node node)
```


Inserts a node into the collection at the specified index.

The node is inserted as a child into the node object from which the collection was created.

If the index is equal to or greater than [getCount()](../../com.aspose.words/nodecollection\#getCount), the node is added at the end of the collection.

If the index is negative and its absolute value is greater than [getCount()](../../com.aspose.words/nodecollection\#getCount), the node is added at the end of the collection.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the node. Negative indexes are allowed and indicate access from the back of the list. For example -1 means the last node, -2 means the second before last and so on. |
| node | [Node](../../com.aspose.words/node) | The node to insert. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Provides a simple "foreach" style iteration over the collection of nodes.

**Returns:**
java.util.Iterator - An Iterator.
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### remove(Node node) {#remove-com.aspose.words.Node}
```
public void remove(Node node)
```


Removes the node from the collection and from the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) | The node to remove. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Removes the node at the specified index from the collection and from the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the node. Negative indexes are allowed and indicate access from the back of the list. For example -1 means the last node, -2 means the second before last and so on. |

### toArray() {#toArray}
```
public Node[] toArray()
```


Copies all nodes from the collection to a new array of nodes.

You should not be adding/removing nodes while iterating over a collection of nodes because it invalidates the iterator and requires refreshes for live collections.

To be able to add/remove nodes during iteration, use this method to copy nodes into a fixed-size array and then iterate over the array.

**Returns:**
com.aspose.words.Node[] - An array of nodes.
### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

