---
title: CompareOptions.AdvancedOptions
linktitle: AdvancedOptions
articleTitle: AdvancedOptions
second_title: Aspose.Words para .NET
description: Descubra CompareOptions AdvancedOptions para optimizar sus comparaciones. Obtenga resultados precisos con configuraciones personalizadas para un resultado óptimo.
type: docs
weight: 20
url: /es/net/aspose.words.comparing/compareoptions/advancedoptions/
---
## CompareOptions.AdvancedOptions property

Especifica opciones de comparación avanzadas que pueden ayudar a producir una salida de comparación más precisa.

```csharp
public AdvancedCompareOptions AdvancedOptions { get; }
```

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

* class [AdvancedCompareOptions](../../advancedcompareoptions/)
* class [CompareOptions](../)
* espacio de nombres [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* asamblea [Aspose.Words](../../../)
