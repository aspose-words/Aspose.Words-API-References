---
title: "AdvancedCompareOptions"
linktitle: "AdvancedCompareOptions"
second_title: "Aspose.Words Java için"
description: "Java'da gelişmiş karşılaştırma seçeneklerini ayarlamayı sağlar."
type: docs
weight: 13
url: /tr/java/com.aspose.words/advancedcompareoptions/
---

**Inheritance:**
java.lang.Object
```
public class AdvancedCompareOptions
```

Gelişmiş karşılaştırma seçeneklerini ayarlamayı sağlar.

 **Remarks:** 

Bu seçeneklerin Microsoft Word'de bir karşılığı yoktur ve daha kesin karşılaştırma sonuçları elde etmeye yardımcı olabilir.

 **Examples:** 

Aynı içeriğe sahip ancak farklı store item kimliğine sahip SDT'yi nasıl karşılaştıracağınızı gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getIgnoreDmlUniqueId()](#getIgnoreDmlUniqueId) | DrawingML benzersiz kimliğindeki farkı yok sayıp saymayacağını belirtir. |
| [getIgnoreStoreItemId()](#getIgnoreStoreItemId) | StructuredDocumentTag depolama öğesi kimliğindeki farkı yok sayıp saymayacağını belirtir. |
| [setIgnoreDmlUniqueId(boolean value)](#setIgnoreDmlUniqueId-boolean) | DrawingML benzersiz kimliğindeki farkı yok sayıp saymayacağını belirtir. |
| [setIgnoreStoreItemId(boolean value)](#setIgnoreStoreItemId-boolean) | StructuredDocumentTag depolama öğesi kimliğindeki farkı yok sayıp saymayacağını belirtir. |
### getIgnoreDmlUniqueId() {#getIgnoreDmlUniqueId}
```
public boolean getIgnoreDmlUniqueId()
```


DrawingML benzersiz kimliğindeki farkı yok sayıp saymayacağını belirtir.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

DML benzersiz kimliğini yok sayarak belgelerin nasıl karşılaştırılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getIgnoreStoreItemId() {#getIgnoreStoreItemId}
```
public boolean getIgnoreStoreItemId()
```


StructuredDocumentTag depolama öğesi kimliğindeki farkı yok sayıp saymayacağını belirtir.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

Aynı içeriğe sahip ancak farklı store item kimliğine sahip SDT'yi nasıl karşılaştıracağınızı gösterir.

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
boolean - İlgili  boolean  değeri.
### setIgnoreDmlUniqueId(boolean value) {#setIgnoreDmlUniqueId-boolean}
```
public void setIgnoreDmlUniqueId(boolean value)
```


DrawingML benzersiz kimliğindeki farkı yok sayıp saymayacağını belirtir.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

DML benzersiz kimliğini yok sayarak belgelerin nasıl karşılaştırılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setIgnoreStoreItemId(boolean value) {#setIgnoreStoreItemId-boolean}
```
public void setIgnoreStoreItemId(boolean value)
```


StructuredDocumentTag depolama öğesi kimliğindeki farkı yok sayıp saymayacağını belirtir.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

Aynı içeriğe sahip ancak farklı store item kimliğine sahip SDT'yi nasıl karşılaştıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

