---
title: RevisionCollection
linktitle: RevisionCollection
second_title: Aspose.Words for Java API Reference
description: A collection of  objects that represent revisions in the document in Java.
type: docs
weight: 490
url: /java/com.aspose.words/revisioncollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class RevisionCollection implements Iterable
```

A collection of [Revision](../../com.aspose.words/revision/) objects that represent revisions in the document.

To learn more, visit the [ Track Changes in a Document ][Track Changes in a Document] documentation article.

You do not create instances of this class directly. Use the [Document.getRevisions()](../../com.aspose.words/document/\#getRevisions) property to get revisions present in a document.


[Track Changes in a Document]: https://docs.aspose.com/words/java/track-changes-in-a-document/
## Methods

| Method | Description |
| --- | --- |
| [acceptAll()](#acceptAll) | Accepts all revisions in this collection. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(int index)](#get-int) | Returns a [Revision](../../com.aspose.words/revision/) at the specified index. |
| [getClass()](#getClass) |  |
| [getCount()](#getCount) | Returns the number of revisions in the collection. |
| [getGroups()](#getGroups) | Collection of revision groups. |
| [hashCode()](#hashCode) |  |
| [iterator()](#iterator) | Returns an enumerator object. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [rejectAll()](#rejectAll) | Rejects all revisions in this collection. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### acceptAll() {#acceptAll}
```
public void acceptAll()
```


Accepts all revisions in this collection.

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
public Revision get(int index)
```


Returns a [Revision](../../com.aspose.words/revision/) at the specified index.

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

**Returns:**
[Revision](../../com.aspose.words/revision/) - A [Revision](../../com.aspose.words/revision/) at the specified index.
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


Returns the number of revisions in the collection.

**Returns:**
int - The number of revisions in the collection.
### getGroups() {#getGroups}
```
public RevisionGroupCollection getGroups()
```


Collection of revision groups.

**Returns:**
[RevisionGroupCollection](../../com.aspose.words/revisiongroupcollection/) - The corresponding [RevisionGroupCollection](../../com.aspose.words/revisiongroupcollection/) value.
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


Returns an enumerator object.

**Returns:**
java.util.Iterator
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### rejectAll() {#rejectAll}
```
public void rejectAll()
```


Rejects all revisions in this collection.

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

