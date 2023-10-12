---
title: ParagraphFormat.KeepWithNext
second_title: Référence de l'API Aspose.Words pour .NET
description: ParagraphFormat propriété. Vrai si le paragraphe doit rester sur la même page que le paragraphe qui le suit.
type: docs
weight: 170
url: /fr/net/aspose.words/paragraphformat/keepwithnext/
---
## ParagraphFormat.KeepWithNext property

Vrai si le paragraphe doit rester sur la même page que le paragraphe qui le suit.

```csharp
public bool KeepWithNext { get; set; }
```

### Exemples

Montre comment dresser une table pour rester ensemble sur la même page.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Activation de KeepWithNext pour chaque paragraphe du tableau à l'exception du
// les derniers de la dernière ligne empêcheront le tableau de se diviser sur plusieurs pages.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true).OfType<Cell>())
    foreach (Paragraph para in cell.Paragraphs.OfType<Paragraph>())
    {
        Assert.True(para.IsInCell);

        if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
            para.ParagraphFormat.KeepWithNext = true;
    }

doc.Save(ArtifactsDir + "Table.KeepTableTogether.docx");
```

### Voir également

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../paragraphformat/)
* Assemblée [Aspose.Words](../../../)


