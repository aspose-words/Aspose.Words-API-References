---
title: DocumentPropertyCollection
second_title: Aspose.Words for Java API Reference
description: Base class for  and  collections.
type: docs
weight: 127
url: /java/com.aspose.words/documentpropertycollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public abstract class DocumentPropertyCollection implements Iterable
```

Base class for [BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties) and [CustomDocumentProperties](../../com.aspose.words/customdocumentproperties) collections.

To learn more, visit the **Work with Document Properties** documentation article.

The names of the properties are case-insensitive.

The properties in the collection are sorted alphabetically by name.
## Constructors

| Constructor | Description |
| --- | --- |
| [DocumentPropertyCollection()](#DocumentPropertyCollection--) |  |
## Methods

| Method | Description |
| --- | --- |
| [getCount()](#getCount--) | Gets number of items in the collection. |
| [get(String name)](#get-java.lang.String-) | Provides access to the collection items. |
| [get(int index)](#get-int-) | Returns a [DocumentProperty](../../com.aspose.words/documentproperty) object by index. |
| [iterator()](#iterator--) | Returns an iterator object that can be used to iterate over all items in the collection. |
| [contains(String name)](#contains-java.lang.String-) | Returns true if a property with the specified name exists in the collection. |
| [indexOf(String name)](#indexOf-java.lang.String-) | Gets the index of a property by name. |
| [remove(String name)](#remove-java.lang.String-) | Removes a property with the specified name from the collection. |
| [removeAt(int index)](#removeAt-int-) | Removes a property at the specified index. |
| [clear()](#clear--) | Removes all properties from the collection. |
### DocumentPropertyCollection() {#DocumentPropertyCollection--}
```
public DocumentPropertyCollection()
```


### getCount() {#getCount--}
```
public int getCount()
```


Gets number of items in the collection.

**Returns:**
int - Number of items in the collection.
### get(String name) {#get-java.lang.String-}
```
public DocumentProperty get(String name)
```


Provides access to the collection items.  Returns a [DocumentProperty](../../com.aspose.words/documentproperty) object by the name of the property.

Returns null if a property with the specified name is not found.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the property to retrieve. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty) - The corresponding [DocumentProperty](../../com.aspose.words/documentproperty) value.
### get(int index) {#get-int-}
```
public DocumentProperty get(int index)
```


Returns a [DocumentProperty](../../com.aspose.words/documentproperty) object by index.

**Note:**  In Java this method is slow because iterates over all nodes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the [DocumentProperty](../../com.aspose.words/documentproperty) to retrieve. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty) - A [DocumentProperty](../../com.aspose.words/documentproperty) object by index.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an iterator object that can be used to iterate over all items in the collection.

**Returns:**
java.util.Iterator
### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


Returns true if a property with the specified name exists in the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the property. |

**Returns:**
boolean - True if the property exists in the collection; false otherwise.
### indexOf(String name) {#indexOf-java.lang.String-}
```
public int indexOf(String name)
```


Gets the index of a property by name.

**Note:**  In Java this method is slow because iterates over all nodes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the property. |

**Returns:**
int - The zero based index. Negative value if not found.
### remove(String name) {#remove-java.lang.String-}
```
public void remove(String name)
```


Removes a property with the specified name from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the property. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Removes a property at the specified index.

**Note:**  In Java this method is slow because iterates over all nodes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero based index. |

### clear() {#clear--}
```
public void clear()
```


Removes all properties from the collection.

