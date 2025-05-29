---
title: RevisionGroup.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words pour .NET
description: Découvrez la propriété RevisionGroup Author pour identifier facilement l'auteur de chaque groupe de révision, améliorant ainsi l'efficacité de votre gestion de documents.
type: docs
weight: 10
url: /fr/net/aspose.words/revisiongroup/author/
---
## RevisionGroup.Author property

Obtient l'auteur de ce groupe de révision.

```csharp
public string Author { get; }
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
