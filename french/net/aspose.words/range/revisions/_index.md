---
title: Range.Revisions
second_title: Référence de l'API Aspose.Words pour .NET
description: Range propriété. Obtient une collection de révisions modifications suivies qui existent dans cette plage.
type: docs
weight: 40
url: /fr/net/aspose.words/range/revisions/
---
## Range.Revisions property

Obtient une collection de révisions (modifications suivies) qui existent dans cette plage.

```csharp
public RevisionCollection Revisions { get; }
```

### Remarques

La collection renvoyée est une collection « live », ce qui signifie que si vous supprimez des parties d'un document contenant des révisions , les révisions supprimées disparaîtront automatiquement de cette collection.

### Exemples

Montre comment travailler avec les révisions dans la plage.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
foreach (Revision revision in paragraph.Range.Revisions)
{
    if (revision.RevisionType == RevisionType.Deletion)
        revision.Accept();
}

// Rejette les révisions de la première section.
doc.FirstSection.Range.Revisions.RejectAll();
```

### Voir également

* class [RevisionCollection](../../revisioncollection/)
* class [Range](../)
* espace de noms [Aspose.Words](../../range/)
* Assemblée [Aspose.Words](../../../)


