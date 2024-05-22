---
title: StructuredDocumentTagCollection
linktitle: StructuredDocumentTagCollection
second_title: Aspose.Words for Java
description: A collection of IStructuredDocumentTag instances that represent the structured document tags in the specified range in Java.
type: docs
weight: 581
url: /java/com.aspose.words/structureddocumenttagcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class StructuredDocumentTagCollection implements Iterable
```

A collection of [IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/) instances that represent the structured document tags in the specified range.

To learn more, visit the [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control] documentation article.


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int) | Returns the structured document tag at the specified index. |
| [getById(int id)](#getById-int) | Returns the structured document tag by identifier. |
| [getByTag(String tag)](#getByTag-java.lang.String) | Returns the first structured document tag encountered in the collection with the specified tag. |
| [getByTitle(String title)](#getByTitle-java.lang.String) | Returns the first structured document tag encountered in the collection with the specified title. |
| [getCount()](#getCount) | Returns the number of structured document tags in the collection. |
| [iterator()](#iterator) | Returns an enumerator object. |
| [remove(int id)](#remove-int) | Removes the structured document tag with the specified identifier. |
| [removeAt(int index)](#removeAt-int) | Removes a structured document tag at the specified index. |
### get(int index) {#get-int}
```
public IStructuredDocumentTag get(int index)
```


Returns the structured document tag at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/) - The structured document tag at the specified index.
### getById(int id) {#getById-int}
```
public IStructuredDocumentTag getById(int id)
```


Returns the structured document tag by identifier.

 **Remarks:** 

Returns null if the structured document tag with the specified identifier cannot be found.

 **Examples:** 

Shows how to get structured document tag.

```

 Document doc = new Document(getMyDir() + "Structured document tags by id.docx");

 // Get the structured document tag by Id.
 IStructuredDocumentTag sdt = doc.getRange().getStructuredDocumentTags().getById(1160505028);
 System.out.println(sdt.isMultiSection());
 System.out.println(sdt.getTitle());

 // Get the structured document tag or ranged tag by Title.
 sdt = doc.getRange().getStructuredDocumentTags().getByTitle("Alias4");
 System.out.println(sdt.getId());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| id | int | The structured document tag identifier. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getByTag(String tag) {#getByTag-java.lang.String}
```
public IStructuredDocumentTag getByTag(String tag)
```


Returns the first structured document tag encountered in the collection with the specified tag.

 **Remarks:** 

Returns null if the structured document tag with the specified tag cannot be found.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tag | java.lang.String | The tag of the structured document tag. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getByTitle(String title) {#getByTitle-java.lang.String}
```
public IStructuredDocumentTag getByTitle(String title)
```


Returns the first structured document tag encountered in the collection with the specified title.

 **Remarks:** 

Returns null if the structured document tag with the specified title cannot be found.

 **Examples:** 

Shows how to get structured document tag.

```

 Document doc = new Document(getMyDir() + "Structured document tags by id.docx");

 // Get the structured document tag by Id.
 IStructuredDocumentTag sdt = doc.getRange().getStructuredDocumentTags().getById(1160505028);
 System.out.println(sdt.isMultiSection());
 System.out.println(sdt.getTitle());

 // Get the structured document tag or ranged tag by Title.
 sdt = doc.getRange().getStructuredDocumentTags().getByTitle("Alias4");
 System.out.println(sdt.getId());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| title | java.lang.String | The title of structured document tag. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getCount() {#getCount}
```
public int getCount()
```


Returns the number of structured document tags in the collection.

**Returns:**
int - The number of structured document tags in the collection.
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an enumerator object.

**Returns:**
java.util.Iterator
### remove(int id) {#remove-int}
```
public void remove(int id)
```


Removes the structured document tag with the specified identifier.

 **Examples:** 

Shows how to remove structured document tag.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 StructuredDocumentTagCollection structuredDocumentTags = doc.getRange().getStructuredDocumentTags();
 IStructuredDocumentTag sdt;
 for (int i = 0; i < structuredDocumentTags.getCount(); i++)
 {
     sdt = structuredDocumentTags.get(i);
     System.out.println(sdt.getTitle());
 }

 sdt = structuredDocumentTags.getById(1691867797);
 Assert.assertEquals(1691867797, sdt.getId());

 Assert.assertEquals(5, structuredDocumentTags.getCount());
 // Remove the structured document tag by Id.
 structuredDocumentTags.remove(1691867797);
 // Remove the structured document tag at position 0.
 structuredDocumentTags.removeAt(0);
 Assert.assertEquals(3, structuredDocumentTags.getCount());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| id | int | The structured document tag identifier. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Removes a structured document tag at the specified index.

 **Examples:** 

Shows how to remove structured document tag.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 StructuredDocumentTagCollection structuredDocumentTags = doc.getRange().getStructuredDocumentTags();
 IStructuredDocumentTag sdt;
 for (int i = 0; i < structuredDocumentTags.getCount(); i++)
 {
     sdt = structuredDocumentTags.get(i);
     System.out.println(sdt.getTitle());
 }

 sdt = structuredDocumentTags.getById(1691867797);
 Assert.assertEquals(1691867797, sdt.getId());

 Assert.assertEquals(5, structuredDocumentTags.getCount());
 // Remove the structured document tag by Id.
 structuredDocumentTags.remove(1691867797);
 // Remove the structured document tag at position 0.
 structuredDocumentTags.removeAt(0);
 Assert.assertEquals(3, structuredDocumentTags.getCount());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

