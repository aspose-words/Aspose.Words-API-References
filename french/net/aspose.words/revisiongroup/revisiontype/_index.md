---
title: RevisionGroup.RevisionType
linktitle: RevisionType
articleTitle: RevisionType
second_title: Aspose.Words pour .NET
description: RevisionGroup RevisionType propriété. Obtient le type de révisions incluses dans ce groupe en C#.
type: docs
weight: 20
url: /fr/net/aspose.words/revisiongroup/revisiontype/
---
## RevisionGroup.RevisionType property

Obtient le type de révisions incluses dans ce groupe.

```csharp
public RevisionType RevisionType { get; }
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

* enum [RevisionType](../../revisiontype/)
* class [RevisionGroup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
