---
title: CustomXmlPartCollection
second_title: Aspose.Words for Java API Reference
description: Represents a collection of Custom XML Parts.
type: docs
weight: 105
url: /java/com.aspose.words/customxmlpartcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class CustomXmlPartCollection implements Iterable
```

Represents a collection of Custom XML Parts. The items are [CustomXmlPart](../../com.aspose.words/customxmlpart) objects.

To learn more, visit the **Structured Document Tags or Content Control** documentation article.

You do not normally need to create instances of this class. You can access custom XML data stored in a document via the [Document.getCustomXmlParts()](../../com.aspose.words/document\#getCustomXmlParts--) / [Document.setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-) property.
## Methods

| Method | Description |
| --- | --- |
| [getCount()](#getCount--) | Gets the number of elements contained in the collection. |
| [get(int index)](#get-int-) | Gets an item at the specified index. |
| [set(int index, CustomXmlPart value)](#set-int-com.aspose.words.CustomXmlPart-) | Sets an item at the specified index. |
| [iterator()](#iterator--) | Returns an iterator object that can be used to iterate over all items in the collection. |
| [add(CustomXmlPart part)](#add-com.aspose.words.CustomXmlPart-) | Adds an item to the collection. |
| [add(String id, String xml)](#add-java.lang.String-java.lang.String-) | Creates a new XML part with the specified XML and adds it to the collection. |
| [removeAt(int index)](#removeAt-int-) | Removes an item at the specified index. |
| [clear()](#clear--) | Removes all elements from the collection. |
| [getById(String id)](#getById-java.lang.String-) | Finds and returns a custom XML part by its identifier. |
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
public CustomXmlPart get(int index)
```


Gets an item at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the item. |

**Returns:**
[CustomXmlPart](../../com.aspose.words/customxmlpart) - An item at the specified index.
### set(int index, CustomXmlPart value) {#set-int-com.aspose.words.CustomXmlPart-}
```
public void set(int index, CustomXmlPart value)
```


Sets an item at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the item. |
| value | [CustomXmlPart](../../com.aspose.words/customxmlpart) | An item at the specified index. |

### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an iterator object that can be used to iterate over all items in the collection.

**Returns:**
java.util.Iterator
### add(CustomXmlPart part) {#add-com.aspose.words.CustomXmlPart-}
```
public void add(CustomXmlPart part)
```


Adds an item to the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| part | [CustomXmlPart](../../com.aspose.words/customxmlpart) | The custom XML part to add. |

### add(String id, String xml) {#add-java.lang.String-java.lang.String-}
```
public CustomXmlPart add(String id, String xml)
```


Creates a new XML part with the specified XML and adds it to the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| id | java.lang.String | Identifier of a new custom XML part. |
| xml | java.lang.String | XML data of the part. |

**Returns:**
[CustomXmlPart](../../com.aspose.words/customxmlpart) - Created custom XML part.
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

### getById(String id) {#getById-java.lang.String-}
```
public CustomXmlPart getById(String id)
```


Finds and returns a custom XML part by its identifier.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| id | java.lang.String | Case-sensitive string that identifies the custom XML part. |

**Returns:**
[CustomXmlPart](../../com.aspose.words/customxmlpart) - Returns  null  if a custom XML part with the specified identifier is not found.
### deepClone() {#deepClone--}
```
public CustomXmlPartCollection deepClone()
```


Makes a deep copy of this collection and its items.

**Returns:**
[CustomXmlPartCollection](../../com.aspose.words/customxmlpartcollection)
