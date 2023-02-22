---
title: RevisionGroupCollection.Item
second_title: Aspose.Words per .NET API Reference
description: RevisionGroupCollection proprietà. Restituisce un gruppo di revisioni in corrispondenza dellindice specificato.
type: docs
weight: 20
url: /it/net/aspose.words/revisiongroupcollection/item/
---
## RevisionGroupCollection indexer

Restituisce un gruppo di revisioni in corrispondenza dell'indice specificato.

```csharp
public RevisionGroup this[int index] { get; }
```

### Esempi

Mostra come ottenere un gruppo di revisioni in un documento.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### Guarda anche

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* spazio dei nomi [Aspose.Words](../../revisiongroupcollection/)
* assemblea [Aspose.Words](../../../)


