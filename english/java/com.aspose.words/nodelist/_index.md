---
title: NodeList
second_title: Aspose.Words for Java API Reference
description: Represents a collection of nodes matching an XPath query executed using the  method.
type: docs
weight: 410
url: /java/com.aspose.words/nodelist/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class NodeList implements Iterable
```

Represents a collection of nodes matching an XPath query executed using the [CompositeNode.selectNodes(java.lang.String)](../../com.aspose.words/compositenode\#selectNodes-java.lang.String) method.

To learn more, visit the [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_] documentation article.

[NodeList](../../com.aspose.words/nodelist) is returned by [CompositeNode.selectNodes(java.lang.String)](../../com.aspose.words/compositenode\#selectNodes-java.lang.String) and contains a collection of nodes matching the XPath query.

[NodeList](../../com.aspose.words/nodelist) supports indexed access and iteration.

Treat the [NodeList](../../com.aspose.words/nodelist) collection as a "snapshot" collection. [NodeList](../../com.aspose.words/nodelist) starts as a "live" collection because the nodes are not actually retrieved when the XPath query is run. The nodes are only retrieved upon access and at this time the node and all nodes that precede it are cached forming a "snapshot" collection.


[Aspose.Words Document Object Model _DOM_]: https://docs.aspose.com/words/java/aspose-words-document-object-model/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(int index)](#get-int) | Retrieves a node at the given index. |
| [getClass()](#getClass) |  |
| [getCount()](#getCount) | Gets the number of nodes in the list. |
| [hashCode()](#hashCode) |  |
| [iterator()](#iterator) | Provides a simple "foreach" style iteration over the collection of nodes. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toArray()](#toArray) | Copies all nodes from the collection to a new array of nodes. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of nodes in the list.

**Returns:**
int - The number of nodes in the list.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
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

