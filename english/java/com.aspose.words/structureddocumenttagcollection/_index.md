---
title: StructuredDocumentTagCollection
second_title: Aspose.Words for Java API Reference
description: A collection of  instances that represent the structured document tags in the specified range.
type: docs
weight: 533
url: /java/com.aspose.words/structureddocumenttagcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class StructuredDocumentTagCollection implements Iterable
```

A collection of [IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag) instances that represent the structured document tags in the specified range.

To learn more, visit the **Structured Document Tags or Content Control** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getById(int id)](#getById-int-) | Returns the structured document tag by identifier. |
| [getByTitle(String title)](#getByTitle-java.lang.String-) | Returns the first structured document tag encountered in the collection with the specified title. |
| [getByTag(String tag)](#getByTag-java.lang.String-) | Returns the first structured document tag encountered in the collection with the specified tag. |
| [remove(int id)](#remove-int-) | Removes the structured document tag with the specified identifier. |
| [removeAt(int index)](#removeAt-int-) | Removes a structured document tag at the specified index. |
| [getCount()](#getCount--) | Returns the number of structured document tags in the collection. |
| [get(int index)](#get-int-) | Returns the structured document tag at the specified index. |
| [iterator()](#iterator--) | Returns an enumerator object. |
### getById(int id) {#getById-int-}
```
public IStructuredDocumentTag getById(int id)
```


Returns the structured document tag by identifier.

Returns null if the structured document tag with the specified identifier cannot be found.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| id | int | The structured document tag identifier. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag)
### getByTitle(String title) {#getByTitle-java.lang.String-}
```
public IStructuredDocumentTag getByTitle(String title)
```


Returns the first structured document tag encountered in the collection with the specified title.

Returns null if the structured document tag with the specified title cannot be found.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| title | java.lang.String | The title of structured document tag. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag)
### getByTag(String tag) {#getByTag-java.lang.String-}
```
public IStructuredDocumentTag getByTag(String tag)
```


Returns the first structured document tag encountered in the collection with the specified tag.

Returns null if the structured document tag with the specified tag cannot be found.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tag | java.lang.String | The tag of the structured document tag. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag)
### remove(int id) {#remove-int-}
```
public void remove(int id)
```


Removes the structured document tag with the specified identifier.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| id | int | The structured document tag identifier. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Removes a structured document tag at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

### getCount() {#getCount--}
```
public int getCount()
```


Returns the number of structured document tags in the collection.

**Returns:**
int - The number of structured document tags in the collection.
### get(int index) {#get-int-}
```
public IStructuredDocumentTag get(int index)
```


Returns the structured document tag at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag) - The structured document tag at the specified index.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an enumerator object.

**Returns:**
java.util.Iterator
