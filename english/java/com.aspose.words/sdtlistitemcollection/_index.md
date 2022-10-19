---
title: SdtListItemCollection
second_title: Aspose.Words for Java API Reference
description: Provides access to  elements of a structured document tag.
type: docs
weight: 507
url: /java/com.aspose.words/sdtlistitemcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class SdtListItemCollection implements Cloneable, Iterable
```

Provides access to [SdtListItem](../../com.aspose.words/sdtlistitem) elements of a structured document tag.

To learn more, visit the **Structured Document Tags or Content Control** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [iterator()](#iterator--) | Returns an iterator object that can be used to iterate over all items in the collection. |
| [add(SdtListItem item)](#add-com.aspose.words.SdtListItem-) | Adds an item to this collection. |
| [removeAt(int index)](#removeAt-int-) | Removes a list item at the specified index. |
| [clear()](#clear--) | Clears all items from this collection. |
| [getSelectedValue()](#getSelectedValue--) | Specifies currently selected value in this list. |
| [setSelectedValue(SdtListItem value)](#setSelectedValue-com.aspose.words.SdtListItem-) | Specifies currently selected value in this list. |
| [get(int index)](#get-int-) | Returns a [SdtListItem](../../com.aspose.words/sdtlistitem) object given its zero-based index in the collection. |
| [getCount()](#getCount--) | Gets number of items in the collection. |
### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an iterator object that can be used to iterate over all items in the collection.

**Returns:**
java.util.Iterator
### add(SdtListItem item) {#add-com.aspose.words.SdtListItem-}
```
public void add(SdtListItem item)
```


Adds an item to this collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| item | [SdtListItem](../../com.aspose.words/sdtlistitem) |  |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Removes a list item at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the item to remove. |

### clear() {#clear--}
```
public void clear()
```


Clears all items from this collection.

### getSelectedValue() {#getSelectedValue--}
```
public SdtListItem getSelectedValue()
```


Specifies currently selected value in this list. Null value allowed, meaning that no currently selected entry is associated with this list item collection.

**Returns:**
[SdtListItem](../../com.aspose.words/sdtlistitem) - The corresponding [SdtListItem](../../com.aspose.words/sdtlistitem) value.
### setSelectedValue(SdtListItem value) {#setSelectedValue-com.aspose.words.SdtListItem-}
```
public void setSelectedValue(SdtListItem value)
```


Specifies currently selected value in this list. Null value allowed, meaning that no currently selected entry is associated with this list item collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [SdtListItem](../../com.aspose.words/sdtlistitem) | The corresponding [SdtListItem](../../com.aspose.words/sdtlistitem) value. |

### get(int index) {#get-int-}
```
public SdtListItem get(int index)
```


Returns a [SdtListItem](../../com.aspose.words/sdtlistitem) object given its zero-based index in the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[SdtListItem](../../com.aspose.words/sdtlistitem) - A [SdtListItem](../../com.aspose.words/sdtlistitem) object given its zero-based index in the collection.
### getCount() {#getCount--}
```
public int getCount()
```


Gets number of items in the collection.

**Returns:**
int - Number of items in the collection.
