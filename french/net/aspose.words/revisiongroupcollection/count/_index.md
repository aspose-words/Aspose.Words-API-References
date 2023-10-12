---
title: RevisionGroupCollection.Count
second_title: Référence de l'API Aspose.Words pour .NET
description: RevisionGroupCollection propriété. Renvoie le nombre de groupes de révisions dans la collection.
type: docs
weight: 10
url: /fr/net/aspose.words/revisiongroupcollection/count/
---
## RevisionGroupCollection.Count property

Renvoie le nombre de groupes de révisions dans la collection.

```csharp
public int Count { get; }
```

### Exemples

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
* espace de noms [Aspose.Words](../../revisiongroupcollection/)
* Assemblée [Aspose.Words](../../../)


