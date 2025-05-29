---
title: Row.IsLastRow
linktitle: IsLastRow
articleTitle: IsLastRow
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Row IsLastRow. Identifiez facilement si une ligne est la dernière d'une table pour une gestion simplifiée des données et une programmation plus efficace.
type: docs
weight: 50
url: /fr/net/aspose.words.tables/row/islastrow/
---
## Row.IsLastRow property

Vrai s'il s'agit de la dernière ligne d'un tableau ; faux sinon.

```csharp
public bool IsLastRow { get; }
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

* class [Row](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
