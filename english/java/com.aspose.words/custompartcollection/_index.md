---
title: CustomPartCollection
second_title: Aspose.Words for Java API Reference
description: Represents a collection of  objects.
type: docs
weight: 103
url: /java/com.aspose.words/custompartcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class CustomPartCollection implements Iterable
```

Represents a collection of [CustomPart](../../com.aspose.words/custompart) objects.

To learn more, visit the **Structured Document Tags or Content Control** documentation article.

You do not normally need to create instances of this class. You access custom parts related to the OOXML package via the [Document.getPackageCustomParts()](../../com.aspose.words/document\#getPackageCustomParts--) / [Document.setPackageCustomParts(com.aspose.words.CustomPartCollection)](../../com.aspose.words/document\#setPackageCustomParts-com.aspose.words.CustomPartCollection-) property.
## Methods

| Method | Description |
| --- | --- |
| [getCount()](#getCount--) | Gets the number of elements contained in the collection. |
| [get(int index)](#get-int-) | Gets an item at the specified index. |
| [set(int index, CustomPart value)](#set-int-com.aspose.words.CustomPart-) | Sets an item at the specified index. |
| [iterator()](#iterator--) | Returns an iterator object that can be used to iterate over all items in the collection. |
| [add(CustomPart part)](#add-com.aspose.words.CustomPart-) | Adds an item to the collection. |
| [removeAt(int index)](#removeAt-int-) | Removes an item at the specified index. |
| [clear()](#clear--) | Removes all elements from the collection. |
| [deepClone()](#deepClone--) | Makes a deep copy of this collection and its items. |
### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of elements contained in the collection.

**Returns:**
int - The number of elements contained in the collection.
### get(int index) {#get-int-}
```
public CustomPart get(int index)
```


Gets an item at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the item. |

**Returns:**
[CustomPart](../../com.aspose.words/custompart) - An item at the specified index.
### set(int index, CustomPart value) {#set-int-com.aspose.words.CustomPart-}
```
public void set(int index, CustomPart value)
```


Sets an item at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the item. |
| value | [CustomPart](../../com.aspose.words/custompart) | An item at the specified index. |

### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an iterator object that can be used to iterate over all items in the collection.

**Returns:**
java.util.Iterator
### add(CustomPart part) {#add-com.aspose.words.CustomPart-}
```
public void add(CustomPart part)
```


Adds an item to the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| part | [CustomPart](../../com.aspose.words/custompart) | The item to add. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Removes an item at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero based index. |

### clear() {#clear--}
```
public void clear()
```


Removes all elements from the collection.

### deepClone() {#deepClone--}
```
public CustomPartCollection deepClone()
```


Makes a deep copy of this collection and its items.

**Returns:**
[CustomPartCollection](../../com.aspose.words/custompartcollection)