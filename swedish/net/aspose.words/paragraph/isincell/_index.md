---
title: Paragraph.IsInCell
linktitle: IsInCell
articleTitle: IsInCell
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Paragraph IsInCell. Avgör enkelt om ett stycke är ett direkt underordnat stycke till en cell, vilket förbättrar dokumentstrukturen och formateringen.
type: docs
weight: 100
url: /sv/net/aspose.words/paragraph/isincell/
---
## Paragraph.IsInCell property

Sant om detta stycke är ett direkt underordnat stycke till[`Cell`](../../../aspose.words.tables/cell/) ; falskt annars.

```csharp
public bool IsInCell { get; }
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

* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
