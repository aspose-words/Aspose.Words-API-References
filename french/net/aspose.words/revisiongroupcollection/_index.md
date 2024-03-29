---
title: RevisionGroupCollection Class
linktitle: RevisionGroupCollection
articleTitle: RevisionGroupCollection
second_title: Aspose.Words pour .NET
description: Aspose.Words.RevisionGroupCollection classe. Une collection deRevisionGroup objets qui représentent les groupes de révision dans le document en C#.
type: docs
weight: 4790
url: /fr/net/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class

Une collection de[`RevisionGroup`](../revisiongroup/) objets qui représentent les groupes de révision dans le document.

Pour en savoir plus, visitez le[Suivre les modifications dans un document](https://docs.aspose.com/words/net/track-changes-in-a-document/) article documentaire.

```csharp
public sealed class RevisionGroupCollection : IEnumerable<RevisionGroup>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/revisiongroupcollection/count/) { get; } | Renvoie le nombre de groupes de révisions dans la collection. |
| [Item](../../aspose.words/revisiongroupcollection/item/) { get; } | Renvoie un groupe de révisions à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetEnumerator](../../aspose.words/revisiongroupcollection/getenumerator/)() | Renvoie un objet énumérateur. |

## Remarques

Vous ne créez pas directement des instances de cette classe. Utilisez le[`Groups`](../revisioncollection/groups/) Propriété pour obtenir les groupes de révision présents dans un document.

## Exemples

Montre comment obtenir un groupe de révisions dans un document.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

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

* class [RevisionGroup](../revisiongroup/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
