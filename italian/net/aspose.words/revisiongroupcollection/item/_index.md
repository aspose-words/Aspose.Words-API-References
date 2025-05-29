---
title: RevisionGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Accedi facilmente a specifici gruppi di revisione con la proprietà RevisionGroupCollection Item. Migliora la gestione dei dati con un'indicizzazione precisa.
type: docs
weight: 20
url: /it/net/aspose.words/revisiongroupcollection/item/
---
## RevisionGroupCollection indexer

Restituisce un gruppo di revisione all'indice specificato.

```csharp
public RevisionGroup this[int index] { get; }
```

## Esempi

Mostra come ottenere un gruppo di revisioni in un documento.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### Guarda anche

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
