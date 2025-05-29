---
title: Paragraph.IsEndOfCell
linktitle: IsEndOfCell
articleTitle: IsEndOfCell
second_title: Aspose.Words för .NET
description: Upptäck egenskapen IsEndOfCell för stycken. Lär dig hur du identifierar om ett stycke är det sista i en cell, vilket förbättrar din dokumentstruktur.
type: docs
weight: 50
url: /sv/net/aspose.words/paragraph/isendofcell/
---
## Paragraph.IsEndOfCell property

Sant om detta stycke är det sista stycket i en[`Cell`](../../../aspose.words.tables/cell/) ; falskt annars.

```csharp
public bool IsEndOfCell { get; }
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
