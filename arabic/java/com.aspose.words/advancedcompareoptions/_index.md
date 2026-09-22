---
title: "AdvancedCompareOptions"
linktitle: "AdvancedCompareOptions"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتعيين خيارات مقارنة متقدمة في Java."
type: docs
weight: 13
url: /ar/java/com.aspose.words/advancedcompareoptions/
---

**Inheritance:**
java.lang.Object
```
public class AdvancedCompareOptions
```

يسمح بتعيين خيارات مقارنة متقدمة.

 **Remarks:** 

ليس لهذه الخيارات ما يعادلها في Microsoft Word وقد تساعد في إنتاج نتيجة مقارنة أكثر دقة.

 **Examples:** 

يوضح كيفية مقارنة SDT ذات المحتوى نفسه ولكن بمعرف عنصر تخزين مختلف.

```

 Document docA = new Document(getMyDir() + "Document with SDT 1.docx");
 Document docB = new Document(getMyDir() + "Document with SDT 2.docx");

 // Configure options to compare SDT with same content but different store item id.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.getAdvancedOptions().setIgnoreStoreItemId(false);

 docA.compare(docB, "user", new Date(), compareOptions);
 Assert.assertEquals(8, docA.getRevisions().getCount());

 compareOptions.getAdvancedOptions().setIgnoreStoreItemId(true);

 docA.getRevisions().rejectAll();
 docA.compare(docB, "user", new Date(), compareOptions);
 Assert.assertEquals(0, docA.getRevisions().getCount());
 
```
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getIgnoreDmlUniqueId()](#getIgnoreDmlUniqueId) | يحدد ما إذا كان يجب تجاهل الاختلاف في معرف فريد لـ DrawingML. |
| [getIgnoreStoreItemId()](#getIgnoreStoreItemId) | يحدد ما إذا كان يجب تجاهل الاختلاف في معرف عنصر التخزين لـ StructuredDocumentTag. |
| [setIgnoreDmlUniqueId(boolean value)](#setIgnoreDmlUniqueId-boolean) | يحدد ما إذا كان يجب تجاهل الاختلاف في معرف فريد لـ DrawingML. |
| [setIgnoreStoreItemId(boolean value)](#setIgnoreStoreItemId-boolean) | يحدد ما إذا كان يجب تجاهل الاختلاف في معرف عنصر التخزين لـ StructuredDocumentTag. |
### getIgnoreDmlUniqueId() {#getIgnoreDmlUniqueId}
```
public boolean getIgnoreDmlUniqueId()
```


يحدد ما إذا كان يجب تجاهل الاختلاف في معرف فريد لـ DrawingML.

 **Remarks:** 

القيمة الافتراضية هي false .

 **Examples:** 

يوضح كيفية مقارنة المستندات مع تجاهل معرف DML الفريد.

```

 Document docA = new Document(getMyDir() + "DML unique ID original.docx");
 Document docB = new Document(getMyDir() + "DML unique ID compare.docx");

 // By default, Aspose.Words do not ignore DML's unique ID, and the revisions count was 2.
 // If we are ignoring DML's unique ID, and revisions count were 0.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.getAdvancedOptions().setIgnoreDmlUniqueId(isIgnoreDmlUniqueId);

 docA.compare(docB, "Aspose.Words", new Date(), compareOptions);

 Assert.assertEquals(isIgnoreDmlUniqueId ? 1 : 3, docA.getRevisions().getCount());
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getIgnoreStoreItemId() {#getIgnoreStoreItemId}
```
public boolean getIgnoreStoreItemId()
```


يحدد ما إذا كان يجب تجاهل الاختلاف في معرف عنصر التخزين لـ StructuredDocumentTag.

 **Remarks:** 

القيمة الافتراضية هي false .

 **Examples:** 

يوضح كيفية مقارنة SDT ذات المحتوى نفسه ولكن بمعرف عنصر تخزين مختلف.

```

 Document docA = new Document(getMyDir() + "Document with SDT 1.docx");
 Document docB = new Document(getMyDir() + "Document with SDT 2.docx");

 // Configure options to compare SDT with same content but different store item id.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.getAdvancedOptions().setIgnoreStoreItemId(false);

 docA.compare(docB, "user", new Date(), compareOptions);
 Assert.assertEquals(8, docA.getRevisions().getCount());

 compareOptions.getAdvancedOptions().setIgnoreStoreItemId(true);

 docA.getRevisions().rejectAll();
 docA.compare(docB, "user", new Date(), compareOptions);
 Assert.assertEquals(0, docA.getRevisions().getCount());
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### setIgnoreDmlUniqueId(boolean value) {#setIgnoreDmlUniqueId-boolean}
```
public void setIgnoreDmlUniqueId(boolean value)
```


يحدد ما إذا كان يجب تجاهل الاختلاف في معرف فريد لـ DrawingML.

 **Remarks:** 

القيمة الافتراضية هي false .

 **Examples:** 

يوضح كيفية مقارنة المستندات مع تجاهل معرف DML الفريد.

```

 Document docA = new Document(getMyDir() + "DML unique ID original.docx");
 Document docB = new Document(getMyDir() + "DML unique ID compare.docx");

 // By default, Aspose.Words do not ignore DML's unique ID, and the revisions count was 2.
 // If we are ignoring DML's unique ID, and revisions count were 0.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.getAdvancedOptions().setIgnoreDmlUniqueId(isIgnoreDmlUniqueId);

 docA.compare(docB, "Aspose.Words", new Date(), compareOptions);

 Assert.assertEquals(isIgnoreDmlUniqueId ? 1 : 3, docA.getRevisions().getCount());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setIgnoreStoreItemId(boolean value) {#setIgnoreStoreItemId-boolean}
```
public void setIgnoreStoreItemId(boolean value)
```


يحدد ما إذا كان يجب تجاهل الاختلاف في معرف عنصر التخزين لـ StructuredDocumentTag.

 **Remarks:** 

القيمة الافتراضية هي false .

 **Examples:** 

يوضح كيفية مقارنة SDT ذات المحتوى نفسه ولكن بمعرف عنصر تخزين مختلف.

```

 Document docA = new Document(getMyDir() + "Document with SDT 1.docx");
 Document docB = new Document(getMyDir() + "Document with SDT 2.docx");

 // Configure options to compare SDT with same content but different store item id.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.getAdvancedOptions().setIgnoreStoreItemId(false);

 docA.compare(docB, "user", new Date(), compareOptions);
 Assert.assertEquals(8, docA.getRevisions().getCount());

 compareOptions.getAdvancedOptions().setIgnoreStoreItemId(true);

 docA.getRevisions().rejectAll();
 docA.compare(docB, "user", new Date(), compareOptions);
 Assert.assertEquals(0, docA.getRevisions().getCount());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

