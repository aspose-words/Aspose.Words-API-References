---
title: Cell.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Cellstycken för att få åtkomst till en samling direkta understycken, vilket förbättrar dokumentets struktur och läsbarhet.
type: docs
weight: 90
url: /sv/net/aspose.words.tables/cell/paragraphs/
---
## Cell.Paragraphs property

Hämtar en samling stycken som är direkta underordnade stycken till cellen.

```csharp
public ParagraphCollection Paragraphs { get; }
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

* class [ParagraphCollection](../../../aspose.words/paragraphcollection/)
* class [Cell](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
