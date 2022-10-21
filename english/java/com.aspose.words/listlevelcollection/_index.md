---
title: ListLevelCollection
second_title: Aspose.Words for Java API Reference
description: A collection of list formatting for each level in a list.
type: docs
weight: 374
url: /java/com.aspose.words/listlevelcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class ListLevelCollection implements Cloneable, Iterable
```

A collection of list formatting for each level in a list.

To learn more, visit the **Working with Lists** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [iterator()](#iterator--) | Gets the enumerator object that will enumerate levels in this list. |
| [get(int index)](#get-int-) | Gets a list level by index. |
| [set(int index, ListLevel value)](#set-int-com.aspose.words.ListLevel-) | Gets a list level by index. |
| [getCount()](#getCount--) | Gets the number of levels in this list. |
### iterator() {#iterator--}
```
public Iterator iterator()
```


Gets the enumerator object that will enumerate levels in this list.

**Returns:**
java.util.Iterator
### get(int index) {#get-int-}
```
public ListLevel get(int index)
```


Gets a list level by index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[ListLevel](../../com.aspose.words/listlevel) - A list level by index.
### set(int index, ListLevel value) {#set-int-com.aspose.words.ListLevel-}
```
public void set(int index, ListLevel value)
```


Gets a list level by index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| value | [ListLevel](../../com.aspose.words/listlevel) | A list level by index. |

### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of levels in this list.

There could be 1 or 9 levels in a list.

**Returns:**
int - The number of levels in this list.
