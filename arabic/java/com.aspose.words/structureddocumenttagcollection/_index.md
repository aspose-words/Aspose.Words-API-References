---
title: "StructuredDocumentTagCollection"
linktitle: "StructuredDocumentTagCollection"
second_title: "Aspose.Words لـ Java"
description: "مجموعة من كائنات IStructuredDocumentTag التي تمثل وسوم المستند المهيكلة في النطاق المحدد في Java."
type: docs
weight: 638
url: /ar/java/com.aspose.words/structureddocumenttagcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class StructuredDocumentTagCollection implements Iterable
```

مجموعة من كائنات [IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/) التي تمثل وسوم المستند المهيكلة في النطاق المحدد.

لمزيد من المعلومات، زر مقالة الوثائق [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Examples:** 

يظهر كيفية الحصول على علامة المستند المهيكلة.

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


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [get(int index)](#get-int) | يعيد وسم المستند المهيكل عند الفهرس المحدد. |
| [getById(int id)](#getById-int) | يعيد وسم المستند المهيكل حسب المعرف. |
| [getByTag(String tag)](#getByTag-java.lang.String) | يعيد أول وسم مستند مهيكل يتم العثور عليه في المجموعة بالوسم المحدد. |
| [getByTitle(String title)](#getByTitle-java.lang.String) | يعيد أول وسم مستند مهيكل يتم العثور عليه في المجموعة بالعنوان المحدد. |
| [getCount()](#getCount) | يعيد عدد وسوم المستند المهيكلة في المجموعة. |
| [iterator()](#iterator) | يرجع كائن عداد. |
| [remove(int id)](#remove-int) | يزيل وسم المستند المهيكل بالمعرف المحدد. |
| [removeAt(int index)](#removeAt-int) | يزيل وسم مستند مهيكل عند الفهرس المحدد. |
### get(int index) {#get-int}
```
public IStructuredDocumentTag get(int index)
```


يعيد وسم المستند المهيكل عند الفهرس المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | فهرس داخل المجموعة. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/) - The structured document tag at the specified index.
### getById(int id) {#getById-int}
```
public IStructuredDocumentTag getById(int id)
```


يعيد وسم المستند المهيكل حسب المعرف.

 **Remarks:** 

يعيد null إذا تعذر العثور على وسم المستند المهيكل بالمعرف المحدد.

 **Examples:** 

يظهر كيفية الحصول على علامة المستند المهيكلة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| id | int | معرف وسم المستند المهيكل. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getByTag(String tag) {#getByTag-java.lang.String}
```
public IStructuredDocumentTag getByTag(String tag)
```


يعيد أول وسم مستند مهيكل يتم العثور عليه في المجموعة بالوسم المحدد.

 **Remarks:** 

يعيد null إذا تعذر العثور على وسم المستند المهيكل بالوسم المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| العلامة | java.lang.String | العلامة الخاصة بعلامة المستند المهيكل. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getByTitle(String title) {#getByTitle-java.lang.String}
```
public IStructuredDocumentTag getByTitle(String title)
```


يعيد أول وسم مستند مهيكل يتم العثور عليه في المجموعة بالعنوان المحدد.

 **Remarks:** 

يعيد null إذا لم يتم العثور على علامة المستند المهيكل ذات العنوان المحدد.

 **Examples:** 

يظهر كيفية الحصول على علامة المستند المهيكلة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| العنوان | java.lang.String | عنوان علامة المستند المهيكل. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getCount() {#getCount}
```
public int getCount()
```


يعيد عدد وسوم المستند المهيكلة في المجموعة.

**Returns:**
int - عدد علامات المستند المهيكل في المجموعة.
### iterator() {#iterator}
```
public Iterator iterator()
```


يرجع كائن عداد.

**Returns:**
java.util.Iterator
### remove(int id) {#remove-int}
```
public void remove(int id)
```


يزيل وسم المستند المهيكل بالمعرف المحدد.

 **Examples:** 

يوضح كيفية إزالة علامة المستند المهيكلة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| id | int | معرف وسم المستند المهيكل. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


يزيل وسم مستند مهيكل عند الفهرس المحدد.

 **Examples:** 

يوضح كيفية إزالة علامة المستند المهيكلة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | فهرس داخل المجموعة. |

