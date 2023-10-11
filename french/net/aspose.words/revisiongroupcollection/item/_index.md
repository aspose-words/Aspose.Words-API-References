---
title: RevisionGroupCollection.Item
second_title: Référence de l'API Aspose.Words pour .NET
description: RevisionGroupCollection propriété. Renvoie un groupe de révisions à lindex spécifié.
type: docs
weight: 20
url: /fr/net/aspose.words/revisiongroupcollection/item/
---
## RevisionGroupCollection indexer

Renvoie un groupe de révisions à l'index spécifié.

```csharp
public RevisionGroup this[int index] { get; }
```

### Exemples

Montre comment obtenir un groupe de révisions dans un document.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### Voir également

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* espace de noms [Aspose.Words](../../revisiongroupcollection/)
* Assemblée [Aspose.Words](../../../)


