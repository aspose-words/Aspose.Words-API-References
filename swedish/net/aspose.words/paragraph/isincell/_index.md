---
title: Paragraph.IsInCell
second_title: Aspose.Words för .NET API Referens
description: Paragraph fast egendom. Sant om det här stycket är ett omedelbart barn tillCell  falskt annars.
type: docs
weight: 100
url: /sv/net/aspose.words/paragraph/isincell/
---
## Paragraph.IsInCell property

Sant om det här stycket är ett omedelbart barn till[`Cell`](../../../aspose.words.tables/cell/) ; falskt annars.

```csharp
public bool IsInCell { get; }
```

### Exempel

Visar hur man ställer in ett bord för att hålla ihop på samma sida.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Aktivera KeepWithNext för varje stycke i tabellen utom för
// de sista i den sista raden kommer att förhindra att tabellen delas upp på flera sidor.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true).OfType<Cell>())
    foreach (Paragraph para in cell.Paragraphs.OfType<Paragraph>())
    {
        Assert.True(para.IsInCell);

        if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
            para.ParagraphFormat.KeepWithNext = true;
    }

doc.Save(ArtifactsDir + "Table.KeepTableTogether.docx");
```

### Se även

* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../paragraph/)
* hopsättning [Aspose.Words](../../../)


