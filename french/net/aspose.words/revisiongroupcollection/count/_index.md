---
title: RevisionGroupCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Count de RevisionGroupCollection. Récupérez facilement le nombre total de groupes de révision et optimisez votre gestion des données.
type: docs
weight: 10
url: /fr/net/aspose.words/revisiongroupcollection/count/
---
## RevisionGroupCollection.Count property

Renvoie le nombre de groupes de révision dans la collection.

```csharp
public int Count { get; }
```

## Exemples

Montre comment imprimer des informations sur un groupe de révisions dans un document.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Assert.AreEqual(7, doc.Revisions.Groups.Count);

foreach (RevisionGroup group in doc.Revisions.Groups)
{
    Console.WriteLine(
        $"Revision author: {group.Author}; Revision type: {group.RevisionType} \n\tRevision text: {group.Text}");
}
```

### Voir également

* class [RevisionGroupCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
