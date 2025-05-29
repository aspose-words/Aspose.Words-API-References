---
title: AdvancedCompareOptions Class
linktitle: AdvancedCompareOptions
articleTitle: AdvancedCompareOptions
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.AdvancedCompareOptions para una potente comparación de documentos. Personalice la configuración para obtener resultados precisos y una mayor productividad.
type: docs
weight: 460
url: /es/net/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class

Permite configurar opciones de comparación avanzadas.

```csharp
public class AdvancedCompareOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [AdvancedCompareOptions](advancedcompareoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/) { get; set; } | Especifica si se debe ignorar la diferencia en el Id. único de DrawingML. |
| [IgnoreStoreItemId](../../aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/) { get; set; } | Especifica si se debe ignorar la diferencia en el Id. del elemento de almacenamiento StructuredDocumentTag. |

## Observaciones

Estas opciones no tienen equivalencia en Microsoft Word y podrían ayudar a producir un resultado de comparación más preciso.

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

* espacio de nombres [Aspose.Words.Comparing](../../aspose.words.comparing/)
* asamblea [Aspose.Words](../../)
