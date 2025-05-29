---
title: Cell.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Paragraphes de cellule pour accéder à une collection de paragraphes enfants directs, améliorant ainsi la structure et la lisibilité de votre document.
type: docs
weight: 90
url: /fr/net/aspose.words.tables/cell/paragraphs/
---
## Cell.Paragraphs property

Obtient une collection de paragraphes qui sont les enfants immédiats de la cellule.

```csharp
public ParagraphCollection Paragraphs { get; }
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

* class [ParagraphCollection](../../../aspose.words/paragraphcollection/)
* class [Cell](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
