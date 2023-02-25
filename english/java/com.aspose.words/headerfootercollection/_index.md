---
title: HeaderFooterCollection
linktitle: HeaderFooterCollection
second_title: Aspose.Words for Java API Reference
description: Provides typed access to  nodes of a in Java.
type: docs
weight: 319
url: /java/com.aspose.words/headerfootercollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.NodeCollection](../../com.aspose.words/nodecollection/)
```
public class HeaderFooterCollection extends NodeCollection
```

Provides typed access to [HeaderFooter](../../com.aspose.words/headerfooter/) nodes of a [Section](../../com.aspose.words/section/).

To learn more, visit the [ Working with Headers and Footers ][Working with Headers and Footers] documentation article.

There can be maximum of one [HeaderFooter](../../com.aspose.words/headerfooter/)

of each [HeaderFooterType](../../com.aspose.words/headerfootertype/) per [Section](../../com.aspose.words/section/).

[HeaderFooter](../../com.aspose.words/headerfooter/) objects can occur in any order in the collection.


[Working with Headers and Footers]: https://docs.aspose.com/words/java/working-with-headers-and-footers/
## Methods

| Method | Description |
| --- | --- |
| [add(Node node)](#add-com.aspose.words.Node) | Adds a node to the end of the collection. |
| [clear()](#clear) | Removes all nodes from this collection and from the document. |
| [contains(Node node)](#contains-com.aspose.words.Node) | Determines whether a node is in the collection. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(int index)](#get-int) | Retrieves a [HeaderFooter](../../com.aspose.words/headerfooter/) at the given index. |
| [getByHeaderFooterType(int headerFooterType)](#getByHeaderFooterType-int) |  |
| [getClass()](#getClass) |  |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Gets the number of nodes in the collection. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [hashCode()](#hashCode) |  |
| [indexOf(Node node)](#indexOf-com.aspose.words.Node) | Returns the zero-based index of the specified node. |
| [insert(int index, Node node)](#insert-int-com.aspose.words.Node) | Inserts a node into the collection at the specified index. |
| [iterator()](#iterator) | Provides a simple "foreach" style iteration over the collection of nodes. |
| [linkToPrevious(boolean isLinkToPrevious)](#linkToPrevious-boolean) | Links or unlinks all headers and footers to the corresponding headers and footers in the previous section. |
| [linkToPrevious(int headerFooterType, boolean isLinkToPrevious)](#linkToPrevious-int-boolean) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove(Node node)](#remove-com.aspose.words.Node) | Removes the node from the collection and from the document. |
| [removeAt(int index)](#removeAt-int) | Removes the node at the specified index from the collection and from the document. |
| [toArray()](#toArray) | Copies all  HeaderFoorter  s from the collection to a new array of  HeaderFoorter  s. |
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
| node | [Node](../../com.aspose.words/node/) | The node to be added to the end of the collection. |

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

This method performs a linear search; therefore, the average execution time is proportional to [getCount()](../../com.aspose.words/nodecollection/\#getCount).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | The node to locate. |

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


Retrieves a [HeaderFooter](../../com.aspose.words/headerfooter/) at the given index.

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

**Returns:**
[Node](../../com.aspose.words/node/) - The corresponding [HeaderFooter](../../com.aspose.words/headerfooter/) value.
### getByHeaderFooterType(int headerFooterType) {#getByHeaderFooterType-int}
```
public HeaderFooter getByHeaderFooterType(int headerFooterType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterType | int |  |

**Returns:**
[HeaderFooter](../../com.aspose.words/headerfooter/)
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
[CompositeNode](../../com.aspose.words/compositenode/)
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
[Node](../../com.aspose.words/node/)
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node}
```
public Node getNextMatchingNode(Node curNode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
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
| node | [Node](../../com.aspose.words/node/) | The node to locate. |

**Returns:**
int - The zero-based index of the node within the collection, if found; otherwise, -1.

This method performs a linear search; therefore, the average execution time is proportional to [getCount()](../../com.aspose.words/nodecollection/\#getCount).
### insert(int index, Node node) {#insert-int-com.aspose.words.Node}
```
public void insert(int index, Node node)
```


Inserts a node into the collection at the specified index.

The node is inserted as a child into the node object from which the collection was created.

If the index is equal to or greater than [getCount()](../../com.aspose.words/nodecollection/\#getCount), the node is added at the end of the collection.

If the index is negative and its absolute value is greater than [getCount()](../../com.aspose.words/nodecollection/\#getCount), the node is added at the end of the collection.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the node. Negative indexes are allowed and indicate access from the back of the list. For example -1 means the last node, -2 means the second before last and so on. |
| node | [Node](../../com.aspose.words/node/) | The node to insert. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Provides a simple "foreach" style iteration over the collection of nodes.

**Returns:**
java.util.Iterator - An Iterator.
### linkToPrevious(boolean isLinkToPrevious) {#linkToPrevious-boolean}
```
public void linkToPrevious(boolean isLinkToPrevious)
```


Links or unlinks all headers and footers to the corresponding headers and footers in the previous section.

If any of the headers or footers do not exist, creates them automatically.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| isLinkToPrevious | boolean | \{ true  to link the headers and footers to the previous section;  false  to unlink them. |

### linkToPrevious(int headerFooterType, boolean isLinkToPrevious) {#linkToPrevious-int-boolean}
```
public void linkToPrevious(int headerFooterType, boolean isLinkToPrevious)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterType | int |  |
| isLinkToPrevious | boolean |  |

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
| node | [Node](../../com.aspose.words/node/) | The node to remove. |

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
public HeaderFooter[] toArray()
```


Copies all  HeaderFoorter  s from the collection to a new array of  HeaderFoorter  s.

**Returns:**
com.aspose.words.HeaderFooter[] - An array of  HeaderFoorter  s.
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

