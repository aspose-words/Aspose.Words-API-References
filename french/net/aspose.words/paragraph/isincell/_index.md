---
title: Paragraph.IsInCell
linktitle: IsInCell
articleTitle: IsInCell
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Paragraph IsInCell. Déterminez facilement si un paragraphe est un enfant direct d'une cellule, améliorant ainsi la structure et la mise en forme de votre document.
type: docs
weight: 100
url: /fr/net/aspose.words/paragraph/isincell/
---
## Paragraph.IsInCell property

Vrai si ce paragraphe est un enfant immédiat de[`Cell`](../../../aspose.words.tables/cell/) ; faux sinon.

```csharp
public bool IsInCell { get; }
```

## Exemples

Montre comment dresser une table pour rester ensemble sur la même page.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Activation de KeepWithNext pour chaque paragraphe du tableau, à l'exception du
// les derniers de la dernière ligne empêcheront le tableau de se diviser sur plusieurs pages.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true))
    foreach (Paragraph para in cell.Paragraphs)
    {
        Assert.True(para.IsInCell);

        if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
            para.ParagraphFormat.KeepWithNext = true;
    }

doc.Save(ArtifactsDir + "Table.KeepTableTogether.docx");
```

### Voir également

* class [Paragraph](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
