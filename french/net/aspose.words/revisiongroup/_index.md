---
title: RevisionGroup Class
linktitle: RevisionGroup
articleTitle: RevisionGroup
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.RevisionGroup, conçue pour gérer et organiser efficacement les objets de révision séquentiels pour une édition simplifiée des documents.
type: docs
weight: 5520
url: /fr/net/aspose.words/revisiongroup/
---
## RevisionGroup class

Représente un groupe de séquences[`Revision`](../revision/) objets.

Pour en savoir plus, visitez le[Suivre les modifications dans un document](https://docs.aspose.com/words/net/track-changes-in-a-document/) article de documentation.

```csharp
public class RevisionGroup
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Author](../../aspose.words/revisiongroup/author/) { get; } | Obtient l'auteur de ce groupe de révision. |
| [RevisionType](../../aspose.words/revisiongroup/revisiontype/) { get; } | Obtient le type de révisions incluses dans ce groupe. |
| [Text](../../aspose.words/revisiongroup/text/) { get; } | Renvoie le texte inséré/supprimé/déplacé ou la description du changement de format. |

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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
