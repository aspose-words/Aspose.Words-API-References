---
title: Row.IsLastRow
linktitle: IsLastRow
articleTitle: IsLastRow
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Row IsLastRow. Identifiera enkelt om en rad är den sista i en tabell för effektiv datahantering och förbättrad programmeringseffektivitet.
type: docs
weight: 50
url: /sv/net/aspose.words.tables/row/islastrow/
---
## Row.IsLastRow property

Sant om detta är den sista raden i en tabell; annars falskt.

```csharp
public bool IsLastRow { get; }
```

## Exempel

Visar hur man dukar ett bord så att det står ihop på samma sida.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Aktiverar KeepWithNext för varje stycke i tabellen förutom
// de sista på den sista raden förhindrar att tabellen delas upp över flera sidor.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true))
    foreach (Paragraph para in cell.Paragraphs)
    {
        Assert.True(para.IsInCell);

        if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
            para.ParagraphFormat.KeepWithNext = true;
    }

doc.Save(ArtifactsDir + "Table.KeepTableTogether.docx");
```

### Se även

* class [Row](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
