---
title: CustomXmlSchemaCollection
second_title: Aspose.Words for Java API Reference
description: A collection of strings that represent XML schemas that are associated with a custom XML part.
type: docs
weight: 108
url: /java/com.aspose.words/customxmlschemacollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class CustomXmlSchemaCollection implements Iterable
```

A collection of strings that represent XML schemas that are associated with a custom XML part.

To learn more, visit the **Structured Document Tags or Content Control** documentation article.

You do not create instances of this class. You access the collection of XML schemas of a custom XML part via the [CustomXmlPart.getSchemas()](../../com.aspose.words/customxmlpart\#getSchemas--) property.
## Methods

| Method | Description |
| --- | --- |
| [getCount()](#getCount--) | Gets the number of elements contained in the collection. |
| [get(int index)](#get-int-) | Gets the element at the specified index. |
| [set(int index, String value)](#set-int-java.lang.String-) | Sets the element at the specified index. |
| [iterator()](#iterator--) | Returns an iterator object that can be used to iterate over all items in the collection. |
| [add(String value)](#add-java.lang.String-) | Adds an item to the collection. |
| [indexOf(String value)](#indexOf-java.lang.String-) | Returns the zero-based index of the specified value in the collection. |
| [remove(String name)](#remove-java.lang.String-) | Removes the specified value from the collection. |
| [removeAt(int index)](#removeAt-int-) | Removes a value at the specified index. |
| [clear()](#clear--) | Removes all elements from the collection. |
| [deepClone()](#deepClone--) | Makes a deep clone of this object. |
### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of elements contained in the collection.

**Returns:**
int - The number of elements contained in the collection.
### get(int index) {#get-int-}
```
public String get(int index)
```


Gets the element at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
java.lang.String - The element at the specified index.
### set(int index, String value) {#set-int-java.lang.String-}
```
public void set(int index, String value)
```


Sets the element at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| value | java.lang.String | The element at the specified index. |

### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an iterator object that can be used to iterate over all items in the collection.

**Returns:**
java.util.Iterator
### add(String value) {#add-java.lang.String-}
```
public void add(String value)
```


Adds an item to the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The item to add. |

### indexOf(String value) {#indexOf-java.lang.String-}
```
public int indexOf(String value)
```


Returns the zero-based index of the specified value in the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The case-sensitive value to locate. |

**Returns:**
int - The zero based index. Negative value if not found.
### remove(String name) {#remove-java.lang.String-}
```
public void remove(String name)
```


Removes the specified value from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-sensitive value to remove. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Removes a value at the specified index.

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
public CustomXmlSchemaCollection deepClone()
```


Makes a deep clone of this object.

**Returns:**
[CustomXmlSchemaCollection](../../com.aspose.words/customxmlschemacollection)
