---
title: Paragraph.IsEndOfCell
linktitle: IsEndOfCell
articleTitle: IsEndOfCell
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IsEndOfCell pour les paragraphes. Apprenez à identifier si un paragraphe est le dernier d'une cellule et à améliorer la structure de votre document.
type: docs
weight: 50
url: /fr/net/aspose.words/paragraph/isendofcell/
---
## Paragraph.IsEndOfCell property

Vrai si ce paragraphe est le dernier paragraphe d'un[`Cell`](../../../aspose.words.tables/cell/) ; faux sinon.

```csharp
public bool IsEndOfCell { get; }
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
