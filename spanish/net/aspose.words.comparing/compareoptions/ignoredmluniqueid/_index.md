---
title: CompareOptions.IgnoreDmlUniqueId
second_title: Referencia de API de Aspose.Words para .NET
description: CompareOptions propiedad. Especifica si se ignora la diferencia en el ID único de DrawingML. El valor predeterminado esFALSO .
type: docs
weight: 60
url: /es/net/aspose.words.comparing/compareoptions/ignoredmluniqueid/
---
## CompareOptions.IgnoreDmlUniqueId property

Especifica si se ignora la diferencia en el ID único de DrawingML. El valor predeterminado es`FALSO` .

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

### Ejemplos

Muestra cómo comparar documentos ignorando el ID único de DML.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// De forma predeterminada, Aspose.Words no ignora el ID único de DML y el recuento de revisiones fue 2.
// Si ignoramos el ID único de DML y el recuento de revisiones fue 0.
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### Ver también

* class [CompareOptions](../)
* espacio de nombres [Aspose.Words.Comparing](../../compareoptions/)
* asamblea [Aspose.Words](../../../)


