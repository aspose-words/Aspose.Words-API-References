---
title: BookmarkCollection
second_title: Aspose.Words for Java API Reference
description: A collection of  objects that represent the bookmarks in the specified range.
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

A collection of [Bookmark](../../com.aspose.words/bookmark) objects that represent the bookmarks in the specified range.

To learn more, visit the **Working with Bookmarks** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getCount()](#getCount--) | Returns the number of bookmarks in the collection. |
| [get(int index)](#get-int-) | Returns a bookmark at the specified index. |
| [get(String bookmarkName)](#get-java.lang.String-) | Returns a bookmark by name. |
| [remove(Bookmark bookmark)](#remove-com.aspose.words.Bookmark-) | Removes the specified bookmark from the document. |
| [remove(String bookmarkName)](#remove-java.lang.String-) | Removes a bookmark with the specified name. |
| [removeAt(int index)](#removeAt-int-) | Removes a bookmark at the specified index. |
| [clear()](#clear--) | Removes all bookmarks from this collection and from the document. |
| [iterator()](#iterator--) | Returns an enumerator object. |
### getCount() {#getCount--}
```
public int getCount()
```


Returns the number of bookmarks in the collection.

**Returns:**
int - The number of bookmarks in the collection.
### get(int index) {#get-int-}
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
[Bookmark](../../com.aspose.words/bookmark) - A bookmark at the specified index.
### get(String bookmarkName) {#get-java.lang.String-}
```
public Bookmark get(String bookmarkName)
```


Returns a bookmark by name.

Returns null if the bookmark with the specified name cannot be found.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Case-insensitive name of the bookmark. |

**Returns:**
[Bookmark](../../com.aspose.words/bookmark) - A bookmark by name.
### remove(Bookmark bookmark) {#remove-com.aspose.words.Bookmark-}
```
public void remove(Bookmark bookmark)
```


Removes the specified bookmark from the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmark | [Bookmark](../../com.aspose.words/bookmark) | The bookmark to remove. |

### remove(String bookmarkName) {#remove-java.lang.String-}
```
public void remove(String bookmarkName)
```


Removes a bookmark with the specified name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | The case-insensitive name of the bookmark to remove. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Removes a bookmark at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the bookmark to remove. |

### clear() {#clear--}
```
public void clear()
```


Removes all bookmarks from this collection and from the document.

### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an enumerator object.

**Returns:**
java.util.Iterator
