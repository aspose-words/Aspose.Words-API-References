---
title: CompareOptions.IgnoreDmlUniqueId
second_title: Referencia de API de Aspose.Words para .NET
description: CompareOptions propiedad. Especifica si se ignorará la diferencia en el ID único de DrawingML. El valor predeterminado es falso .
type: docs
weight: 50
url: /es/net/aspose.words.comparing/compareoptions/ignoredmluniqueid/
---
## CompareOptions.IgnoreDmlUniqueId property

Especifica si se ignorará la diferencia en el ID único de DrawingML. El valor predeterminado es **falso** .

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

### Ejemplos

Muestra cómo comparar documentos ignorando la ID única de DML.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// De forma predeterminada, Aspose.Words no ignora la ID única de DML y el recuento de revisiones fue de 2.
// Si ignoramos la ID única de DML y el recuento de revisiones fue 0.
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### Ver también

* class [CompareOptions](../)
* espacio de nombres [Aspose.Words.Comparing](../../compareoptions/)
* asamblea [Aspose.Words](../../../)


