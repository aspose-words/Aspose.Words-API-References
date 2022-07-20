---
title: Item
second_title: Referencia de API de Aspose.Words para .NET
description: Devuelve un grupo de revisión en el índice especificado.
type: docs
weight: 20
url: /es/net/aspose.words/revisiongroupcollection/item/
---
## RevisionGroupCollection indexer

Devuelve un grupo de revisión en el índice especificado.

```csharp
public RevisionGroup this[int index] { get; }
```

### Ejemplos

Muestra cómo obtener un grupo de revisiones en un documento.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### Ver también

* class [RevisionGroup](../../revisiongroup)
* class [RevisionGroupCollection](../../revisiongroupcollection)
* espacio de nombres [Aspose.Words](../../revisiongroupcollection)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->