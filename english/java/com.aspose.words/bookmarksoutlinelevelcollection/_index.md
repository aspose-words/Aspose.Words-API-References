---
title: BookmarksOutlineLevelCollection
second_title: Aspose.Words for Java API Reference
description: A collection of individual bookmarks outline level.
type: docs
weight: 35
url: /java/com.aspose.words/bookmarksoutlinelevelcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BookmarksOutlineLevelCollection implements Iterable
```

A collection of individual bookmarks outline level.

To learn more, visit the **Working with Bookmarks** documentation article.

Key is a case-insensitive string bookmark name. Value is a int bookmark outline level.

Bookmark outline level may be a value from 0 to 9. Specify 0 and Word bookmark will not be displayed in the document outline. Specify 1 and Word bookmark will be displayed in the document outline at level 1; 2 for level 2 and so on.
## Methods

| Method | Description |
| --- | --- |
| [getCount()](#getCount--) | Gets the number of elements contained in the collection. |
| [get(String name)](#get-java.lang.String-) | Provides access to the collection items. |
| [set(String name, int value)](#set-java.lang.String-int-) | Provides access to the collection items. |
| [get(int index)](#get-int-) | Gets a bookmark outline level at the specified index. |
| [set(int index, int value)](#set-int-int-) | Sets a bookmark outline level at the specified index. |
| [add(String name, int outlineLevel)](#add-java.lang.String-int-) | Adds a bookmark to the collection. |
| [contains(String name)](#contains-java.lang.String-) | Determines whether the collection contains a bookmark with the given name. |
| [indexOfKey(String name)](#indexOfKey-java.lang.String-) | Returns the zero-based index of the specified bookmark in the collection. |
| [remove(String name)](#remove-java.lang.String-) | Removes a bookmark with the specified name from the collection. |
| [removeAt(int index)](#removeAt-int-) | Removes a bookmark at the specified index. |
| [clear()](#clear--) | Removes all elements from the collection. |
| [iterator()](#iterator--) |  |
### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of elements contained in the collection.

**Returns:**
int - The number of elements contained in the collection.
### get(String name) {#get-java.lang.String-}
```
public int get(String name)
```


Provides access to the collection items.  Gets or a sets a bookmark outline level by the bookmark name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | Case-insensitive name of the bookmark. |

**Returns:**
int - The outline level of the bookmark. Valid range is 0 to 9.
### set(String name, int value) {#set-java.lang.String-int-}
```
public void set(String name, int value)
```


Provides access to the collection items.  Gets or a sets a bookmark outline level by the bookmark name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | Case-insensitive name of the bookmark. |
| value | int | The outline level of the bookmark. Valid range is 0 to 9. |

### get(int index) {#get-int-}
```
public int get(int index)
```


Gets a bookmark outline level at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the bookmark. |

**Returns:**
int - The outline level of the bookmark. Valid range is 0 to 9.
### set(int index, int value) {#set-int-int-}
```
public void set(int index, int value)
```


Sets a bookmark outline level at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the bookmark. |
| value | int | The outline level of the bookmark. Valid range is 0 to 9. |

### add(String name, int outlineLevel) {#add-java.lang.String-int-}
```
public void add(String name, int outlineLevel)
```


Adds a bookmark to the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the bookmark to add. |
| outlineLevel | int | The outline level of the bookmark. Valid range is 0 to 9. |

### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


Determines whether the collection contains a bookmark with the given name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | Case-insensitive name of the bookmark to locate. |

**Returns:**
boolean - True if item is found in the collection; otherwise, false.
### indexOfKey(String name) {#indexOfKey-java.lang.String-}
```
public int indexOfKey(String name)
```


Returns the zero-based index of the specified bookmark in the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the bookmark. |

**Returns:**
int - The zero based index. Negative value if not found.
### remove(String name) {#remove-java.lang.String-}
```
public void remove(String name)
```


Removes a bookmark with the specified name from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the bookmark. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Removes a bookmark at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero based index. |

### clear() {#clear--}
```
public void clear()
```


Removes all elements from the collection.

### iterator() {#iterator--}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator