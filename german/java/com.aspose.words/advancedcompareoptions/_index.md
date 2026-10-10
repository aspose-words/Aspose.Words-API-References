---
title: "AdvancedCompareOptions"
linktitle: "AdvancedCompareOptions"
second_title: "Aspose.Words für Java"
description: "Ermöglicht das Festlegen erweiterter Vergleichsoptionen in Java."
type: docs
weight: 13
url: /de/java/com.aspose.words/advancedcompareoptions/
---

**Inheritance:**
java.lang.Object
```
public class AdvancedCompareOptions
```

Ermöglicht das Festlegen erweiterter Vergleichsoptionen.

 **Remarks:** 

Diese Optionen haben keine Entsprechung in Microsoft Word und können dabei helfen, ein genaueres Vergleichsergebnis zu erzielen.

 **Examples:** 

Zeigt, wie man SDT mit demselben Inhalt, aber unterschiedlicher Store-Element-ID vergleicht.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getIgnoreDmlUniqueId()](#getIgnoreDmlUniqueId) | Gibt an, ob Unterschiede in der eindeutigen DrawingML‑ID ignoriert werden sollen. |
| [getIgnoreStoreItemId()](#getIgnoreStoreItemId) | Gibt an, ob Unterschiede in der Store‑Element-ID des StructuredDocumentTag ignoriert werden sollen. |
| [setIgnoreDmlUniqueId(boolean value)](#setIgnoreDmlUniqueId-boolean) | Gibt an, ob Unterschiede in der eindeutigen DrawingML‑ID ignoriert werden sollen. |
| [setIgnoreStoreItemId(boolean value)](#setIgnoreStoreItemId-boolean) | Gibt an, ob Unterschiede in der Store‑Element-ID des StructuredDocumentTag ignoriert werden sollen. |
### getIgnoreDmlUniqueId() {#getIgnoreDmlUniqueId}
```
public boolean getIgnoreDmlUniqueId()
```


Gibt an, ob Unterschiede in der eindeutigen DrawingML‑ID ignoriert werden sollen.

 **Remarks:** 

Standardwert ist false.

 **Examples:** 

Zeigt, wie man Dokumente vergleicht, wobei die eindeutige DML‑ID ignoriert wird.

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
boolean - Der entsprechende  boolean  Wert.
### getIgnoreStoreItemId() {#getIgnoreStoreItemId}
```
public boolean getIgnoreStoreItemId()
```


Gibt an, ob Unterschiede in der Store‑Element-ID des StructuredDocumentTag ignoriert werden sollen.

 **Remarks:** 

Standardwert ist false.

 **Examples:** 

Zeigt, wie man SDT mit demselben Inhalt, aber unterschiedlicher Store-Element-ID vergleicht.

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
boolean - Der entsprechende  boolean  Wert.
### setIgnoreDmlUniqueId(boolean value) {#setIgnoreDmlUniqueId-boolean}
```
public void setIgnoreDmlUniqueId(boolean value)
```


Gibt an, ob Unterschiede in der eindeutigen DrawingML‑ID ignoriert werden sollen.

 **Remarks:** 

Standardwert ist false.

 **Examples:** 

Zeigt, wie man Dokumente vergleicht, wobei die eindeutige DML‑ID ignoriert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setIgnoreStoreItemId(boolean value) {#setIgnoreStoreItemId-boolean}
```
public void setIgnoreStoreItemId(boolean value)
```


Gibt an, ob Unterschiede in der Store‑Element-ID des StructuredDocumentTag ignoriert werden sollen.

 **Remarks:** 

Standardwert ist false.

 **Examples:** 

Zeigt, wie man SDT mit demselben Inhalt, aber unterschiedlicher Store-Element-ID vergleicht.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

