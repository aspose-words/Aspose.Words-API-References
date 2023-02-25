---
title: BookmarkCollection
linktitle: BookmarkCollection
second_title: Aspose.Words for Java API Reference
description: A collection of  objects that represent the bookmarks in the specified range in Java.
type: docs
weight: 32
url: /java/com.aspose.words/bookmarkcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BookmarkCollection implements Iterable
```

A collection of [Bookmark](../../com.aspose.words/bookmark/) objects that represent the bookmarks in the specified range.

To learn more, visit the [ Working with Bookmarks ][Working with Bookmarks] documentation article.


[Working with Bookmarks]: https://docs.aspose.com/words/java/working-with-bookmarks/
## Methods

| Method | Description |
| --- | --- |
| [clear()](#clear) | Removes all bookmarks from this collection and from the document. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(int index)](#get-int) | Returns a bookmark at the specified index. |
| [get(String bookmarkName)](#get-java.lang.String) | Returns a bookmark by name. |
| [getClass()](#getClass) |  |
| [getCount()](#getCount) | Returns the number of bookmarks in the collection. |
| [hashCode()](#hashCode) |  |
| [iterator()](#iterator) | Returns an enumerator object. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove(Bookmark bookmark)](#remove-com.aspose.words.Bookmark) | Removes the specified bookmark from the document. |
| [remove(String bookmarkName)](#remove-java.lang.String) | Removes a bookmark with the specified name. |
| [removeAt(int index)](#removeAt-int) | Removes a bookmark at the specified index. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### clear() {#clear}
```
public void clear()
```


Removes all bookmarks from this collection and from the document.

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
public Bookmark get(int index)
```


Returns a bookmark at the specified index.

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

**Returns:**
[Bookmark](../../com.aspose.words/bookmark/) - A bookmark at the specified index.
### get(String bookmarkName) {#get-java.lang.String}
```
public Bookmark get(String bookmarkName)
```


Returns a bookmark by name.

Returns  null  if the bookmark with the specified name cannot be found.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Case-insensitive name of the bookmark. |

**Returns:**
[Bookmark](../../com.aspose.words/bookmark/) - A bookmark by name.
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


Returns the number of bookmarks in the collection.

**Returns:**
int - The number of bookmarks in the collection.
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




### remove(Bookmark bookmark) {#remove-com.aspose.words.Bookmark}
```
public void remove(Bookmark bookmark)
```


Removes the specified bookmark from the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmark | [Bookmark](../../com.aspose.words/bookmark/) | The bookmark to remove. |

### remove(String bookmarkName) {#remove-java.lang.String}
```
public void remove(String bookmarkName)
```


Removes a bookmark with the specified name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | The case-insensitive name of the bookmark to remove. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Removes a bookmark at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the bookmark to remove. |

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

