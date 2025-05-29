---
title: ParagraphFormat.KeepWithNext
linktitle: KeepWithNext
articleTitle: KeepWithNext
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété KeepWithNext de ParagraphFormat garantit que vos paragraphes restent ensemble, améliorant ainsi le flux et la lisibilité du document pour un aspect soigné.
type: docs
weight: 170
url: /fr/net/aspose.words/paragraphformat/keepwithnext/
---
## ParagraphFormat.KeepWithNext property

Vrai si le paragraphe doit rester sur la même page que le paragraphe qui le suit.

```csharp
public bool KeepWithNext { get; set; }
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

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
