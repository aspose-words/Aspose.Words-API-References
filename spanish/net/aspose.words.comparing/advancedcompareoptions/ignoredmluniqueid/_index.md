---
title: AdvancedCompareOptions.IgnoreDmlUniqueId
linktitle: IgnoreDmlUniqueId
articleTitle: IgnoreDmlUniqueId
second_title: Aspose.Words para .NET
description: Descubra la propiedad IgnoreDmlUniqueId de AdvancedCompareOptions para optimizar el procesamiento de DrawingML mediante la gestión eficiente de identificadores únicos. ¡Optimice su flujo de trabajo!
type: docs
weight: 20
url: /es/net/aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/
---
## AdvancedCompareOptions.IgnoreDmlUniqueId property

Especifica si se debe ignorar la diferencia en el Id. único de DrawingML.

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO` .

## Ejemplos

Muestra cómo comparar documentos ignorando el ID único de DML.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// De forma predeterminada, Aspose.Words no ignora el ID único de DML y el recuento de revisiones fue 2.
// Si ignoramos el ID único de DML y el recuento de revisiones fuera 0.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### Ver también

* class [AdvancedCompareOptions](../)
* espacio de nombres [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* asamblea [Aspose.Words](../../../)
