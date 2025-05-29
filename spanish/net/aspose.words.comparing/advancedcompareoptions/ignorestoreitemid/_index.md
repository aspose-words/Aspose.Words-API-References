---
title: AdvancedCompareOptions.IgnoreStoreItemId
linktitle: IgnoreStoreItemId
articleTitle: IgnoreStoreItemId
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad IgnoreStoreItemId de AdvancedCompareOptions mejora la comparación de documentos al ignorar las diferencias de ID de StructuredDocumentTag para lograr una mayor precisión.
type: docs
weight: 30
url: /es/net/aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/
---
## AdvancedCompareOptions.IgnoreStoreItemId property

Especifica si se debe ignorar la diferencia en el Id. del elemento de almacenamiento StructuredDocumentTag.

```csharp
public bool IgnoreStoreItemId { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO` .

## Ejemplos

Muestra cómo comparar SDT con el mismo contenido pero con diferentes identificaciones de elementos de la tienda.

```csharp
Document docA = new Document(MyDir + "Document with SDT 1.docx");
Document docB = new Document(MyDir + "Document with SDT 2.docx");

// Configure las opciones para comparar SDT con el mismo contenido pero con diferentes identificaciones de elementos de la tienda.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreStoreItemId = false;

docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(8, docA.Revisions.Count);

compareOptions.AdvancedOptions.IgnoreStoreItemId = true;

docA.Revisions.RejectAll();
docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(0, docA.Revisions.Count);
```

### Ver también

* class [AdvancedCompareOptions](../)
* espacio de nombres [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* asamblea [Aspose.Words](../../../)
