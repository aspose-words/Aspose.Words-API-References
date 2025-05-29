---
title: RevisionGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words para .NET
description: Acceda fácilmente a grupos de revisiones específicos con la propiedad Elemento RevisionGroupCollection. Mejore la gestión de sus datos con una indexación precisa.
type: docs
weight: 20
url: /es/net/aspose.words/revisiongroupcollection/item/
---
## RevisionGroupCollection indexer

Devuelve un grupo de revisión en el índice especificado.

```csharp
public RevisionGroup this[int index] { get; }
```

## Ejemplos

Muestra cómo obtener un grupo de revisiones en un documento.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### Ver también

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
