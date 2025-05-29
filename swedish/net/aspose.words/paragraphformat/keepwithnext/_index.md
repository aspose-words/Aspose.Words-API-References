---
title: ParagraphFormat.KeepWithNext
linktitle: KeepWithNext
articleTitle: KeepWithNext
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen ParagraphFormat KeepWithNext säkerställer att dina stycken hålls ihop, vilket förbättrar dokumentflödet och läsbarheten för ett elegant utseende.
type: docs
weight: 170
url: /sv/net/aspose.words/paragraphformat/keepwithnext/
---
## ParagraphFormat.KeepWithNext property

Sant om stycket ska förbli på samma sida som stycket som följer det.

```csharp
public bool KeepWithNext { get; set; }
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

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
