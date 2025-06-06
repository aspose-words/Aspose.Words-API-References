---
title: RevisionGroup.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words pour .NET
description: Explorez la propriété Texte RevisionGroup pour accéder au texte inséré, supprimé ou déplacé, améliorant ainsi les informations de mise en forme et l'efficacité de l'édition de votre document.
type: docs
weight: 30
url: /fr/net/aspose.words/revisiongroup/text/
---
## RevisionGroup.Text property

Renvoie le texte inséré/supprimé/déplacé ou la description du changement de format.

```csharp
public string Text { get; }
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

* class [RevisionGroup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
