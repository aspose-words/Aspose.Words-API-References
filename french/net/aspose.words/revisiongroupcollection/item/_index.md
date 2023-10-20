---
title: RevisionGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words pour .NET
description: RevisionGroupCollection Item propriété. Renvoie un groupe de révisions à lindex spécifié en C#.
type: docs
weight: 20
url: /fr/net/aspose.words/revisiongroupcollection/item/
---
## RevisionGroupCollection indexer

Renvoie un groupe de révisions à l'index spécifié.

```csharp
public RevisionGroup this[int index] { get; }
```

## Exemples

Montre comment obtenir un groupe de révisions dans un document.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### Voir également

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
