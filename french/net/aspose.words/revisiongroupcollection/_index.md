---
title: RevisionGroupCollection Class
linktitle: RevisionGroupCollection
articleTitle: RevisionGroupCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.RevisionGroupCollection, offrant une gestion efficace des groupes de révision de documents pour une édition et une collaboration améliorées.
type: docs
weight: 5530
url: /fr/net/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class

Une collection de[`RevisionGroup`](../revisiongroup/)objets qui représentent des groupes de révision dans le document.

Pour en savoir plus, visitez le[Suivre les modifications dans un document](https://docs.aspose.com/words/net/track-changes-in-a-document/) article de documentation.

```csharp
public sealed class RevisionGroupCollection : IEnumerable<RevisionGroup>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/revisiongroupcollection/count/) { get; } | Renvoie le nombre de groupes de révision dans la collection. |
| [Item](../../aspose.words/revisiongroupcollection/item/) { get; } | Renvoie un groupe de révision à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetEnumerator](../../aspose.words/revisiongroupcollection/getenumerator/)() | Renvoie un objet énumérateur. |

## Remarques

Vous ne créez pas d'instances de cette classe directement. Utilisez le[`Groups`](../revisioncollection/groups/) Propriété pour obtenir les groupes de révision présents dans un document.

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
