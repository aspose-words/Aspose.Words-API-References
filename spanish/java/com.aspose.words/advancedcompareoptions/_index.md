---
title: "AdvancedCompareOptions"
linktitle: "AdvancedCompareOptions"
second_title: "Aspose.Words para Java"
description: "Permite establecer opciones avanzadas de comparación en Java."
type: docs
weight: 13
url: /es/java/com.aspose.words/advancedcompareoptions/
---

**Inheritance:**
java.lang.Object
```
public class AdvancedCompareOptions
```

Permite establecer opciones avanzadas de comparación.

 **Remarks:** 

Estas opciones no tienen equivalencia en Microsoft Word y pueden ayudar a producir un resultado de comparación más preciso.

 **Examples:** 

Muestra cómo comparar SDT con el mismo contenido pero con un ID de elemento de almacén diferente.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getIgnoreDmlUniqueId()](#getIgnoreDmlUniqueId) | Especifica si se debe ignorar la diferencia en el Id único de DrawingML. |
| [getIgnoreStoreItemId()](#getIgnoreStoreItemId) | Especifica si se debe ignorar la diferencia en el Id del elemento almacenado de StructuredDocumentTag. |
| [setIgnoreDmlUniqueId(boolean value)](#setIgnoreDmlUniqueId-boolean) | Especifica si se debe ignorar la diferencia en el Id único de DrawingML. |
| [setIgnoreStoreItemId(boolean value)](#setIgnoreStoreItemId-boolean) | Especifica si se debe ignorar la diferencia en el Id del elemento almacenado de StructuredDocumentTag. |
### getIgnoreDmlUniqueId() {#getIgnoreDmlUniqueId}
```
public boolean getIgnoreDmlUniqueId()
```


Especifica si se debe ignorar la diferencia en el Id único de DrawingML.

 **Remarks:** 

El valor predeterminado es false.

 **Examples:** 

Muestra cómo comparar documentos ignorando el ID único de DML.

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
boolean - El valor  boolean  correspondiente.
### getIgnoreStoreItemId() {#getIgnoreStoreItemId}
```
public boolean getIgnoreStoreItemId()
```


Especifica si se debe ignorar la diferencia en el Id del elemento almacenado de StructuredDocumentTag.

 **Remarks:** 

El valor predeterminado es false.

 **Examples:** 

Muestra cómo comparar SDT con el mismo contenido pero con un ID de elemento de almacén diferente.

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
boolean - El valor  boolean  correspondiente.
### setIgnoreDmlUniqueId(boolean value) {#setIgnoreDmlUniqueId-boolean}
```
public void setIgnoreDmlUniqueId(boolean value)
```


Especifica si se debe ignorar la diferencia en el Id único de DrawingML.

 **Remarks:** 

El valor predeterminado es false.

 **Examples:** 

Muestra cómo comparar documentos ignorando el ID único de DML.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setIgnoreStoreItemId(boolean value) {#setIgnoreStoreItemId-boolean}
```
public void setIgnoreStoreItemId(boolean value)
```


Especifica si se debe ignorar la diferencia en el Id del elemento almacenado de StructuredDocumentTag.

 **Remarks:** 

El valor predeterminado es false.

 **Examples:** 

Muestra cómo comparar SDT con el mismo contenido pero con un ID de elemento de almacén diferente.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

