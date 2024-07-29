---
title: AdvancedCompareOptions
linktitle: AdvancedCompareOptions
second_title: Aspose.Words for Java
description: Allows to set advanced compare options in Java.
type: docs
weight: 13
url: /java/com.aspose.words/advancedcompareoptions/
---

**Inheritance:**
java.lang.Object
```
public class AdvancedCompareOptions
```

Allows to set advanced compare options.

 **Remarks:** 

These options have no equivalence in Microsoft Word and might help to produce more precise comparison result.

 **Examples:** 

Shows how to compare SDT with same content but different store item id.

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
## Methods

| Method | Description |
| --- | --- |
| [getIgnoreDmlUniqueId()](#getIgnoreDmlUniqueId) | Specifies whether to ignore difference in DrawingML unique Id. |
| [getIgnoreStoreItemId()](#getIgnoreStoreItemId) | Specifies whether to ignore difference in StructuredDocumentTag store item Id. |
| [setIgnoreDmlUniqueId(boolean value)](#setIgnoreDmlUniqueId-boolean) | Specifies whether to ignore difference in DrawingML unique Id. |
| [setIgnoreStoreItemId(boolean value)](#setIgnoreStoreItemId-boolean) | Specifies whether to ignore difference in StructuredDocumentTag store item Id. |
### getIgnoreDmlUniqueId() {#getIgnoreDmlUniqueId}
```
public boolean getIgnoreDmlUniqueId()
```


Specifies whether to ignore difference in DrawingML unique Id.

 **Remarks:** 

Default value is  false .

 **Examples:** 

Shows how to compare documents ignoring DML unique ID.

```

 Document docA = new Document(getMyDir() + "DML unique ID original.docx");
 Document docB = new Document(getMyDir() + "DML unique ID compare.docx");

 // By default, Aspose.Words do not ignore DML's unique ID, and the revisions count was 2.
 // If we are ignoring DML's unique ID, and revisions count were 0.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.getAdvancedOptions().setIgnoreDmlUniqueId(isIgnoreDmlUniqueId);

 docA.compare(docB, "Aspose.Words", new Date(), compareOptions);

 Assert.assertEquals(isIgnoreDmlUniqueId ? 0 : 2, docA.getRevisions().getCount());
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getIgnoreStoreItemId() {#getIgnoreStoreItemId}
```
public boolean getIgnoreStoreItemId()
```


Specifies whether to ignore difference in StructuredDocumentTag store item Id.

 **Remarks:** 

Default value is  false .

 **Examples:** 

Shows how to compare SDT with same content but different store item id.

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
boolean - The corresponding  boolean  value.
### setIgnoreDmlUniqueId(boolean value) {#setIgnoreDmlUniqueId-boolean}
```
public void setIgnoreDmlUniqueId(boolean value)
```


Specifies whether to ignore difference in DrawingML unique Id.

 **Remarks:** 

Default value is  false .

 **Examples:** 

Shows how to compare documents ignoring DML unique ID.

```

 Document docA = new Document(getMyDir() + "DML unique ID original.docx");
 Document docB = new Document(getMyDir() + "DML unique ID compare.docx");

 // By default, Aspose.Words do not ignore DML's unique ID, and the revisions count was 2.
 // If we are ignoring DML's unique ID, and revisions count were 0.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.getAdvancedOptions().setIgnoreDmlUniqueId(isIgnoreDmlUniqueId);

 docA.compare(docB, "Aspose.Words", new Date(), compareOptions);

 Assert.assertEquals(isIgnoreDmlUniqueId ? 0 : 2, docA.getRevisions().getCount());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setIgnoreStoreItemId(boolean value) {#setIgnoreStoreItemId-boolean}
```
public void setIgnoreStoreItemId(boolean value)
```


Specifies whether to ignore difference in StructuredDocumentTag store item Id.

 **Remarks:** 

Default value is  false .

 **Examples:** 

Shows how to compare SDT with same content but different store item id.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

