---
title: BaseWebExtensionCollection
second_title: Aspose.Words for Java API Reference
description: Base class for    and  collections.
type: docs
weight: 27
url: /java/com.aspose.words/basewebextensioncollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public abstract class BaseWebExtensionCollection implements Iterable
```

Base class for [TaskPaneCollection](../../com.aspose.words/taskpanecollection), [WebExtensionBindingCollection](../../com.aspose.words/webextensionbindingcollection), [WebExtensionPropertyCollection](../../com.aspose.words/webextensionpropertycollection) and [WebExtensionReferenceCollection](../../com.aspose.words/webextensionreferencecollection) collections.

To learn more, visit the **Work with Office Add-ins** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [BaseWebExtensionCollection()](#BaseWebExtensionCollection--) |  |
## Methods

| Method | Description |
| --- | --- |
| [getCount()](#getCount--) | Gets the number of elements contained in the collection. |
| [get(int index)](#get-int-) | Gets an item at the specified index. |
| [clear()](#clear--) | Removes all elements from the collection. |
| [remove(int index)](#remove-int-) | Removes the item at the specified index from the collection. |
| [iterator()](#iterator--) | Returns an enumerator that can iterate through a collection. |
### BaseWebExtensionCollection() {#BaseWebExtensionCollection--}
```
public BaseWebExtensionCollection()
```


### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of elements contained in the collection.

**Returns:**
int - The number of elements contained in the collection.
### get(int index) {#get-int-}
```
public Object get(int index)
```


Gets an item at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the item. |

**Returns:**
java.lang.Object - An item at the specified index.
### clear() {#clear--}
```
public void clear()
```


Removes all elements from the collection.

### remove(int index) {#remove-int-}
```
public void remove(int index)
```


Removes the item at the specified index from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the collection item. |

### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an enumerator that can iterate through a collection.

**Returns:**
java.util.Iterator - 
