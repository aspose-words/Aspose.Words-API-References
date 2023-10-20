---
title: Cell.ParentRow
linktitle: ParentRow
articleTitle: ParentRow
second_title: Aspose.Words för .NET
description: Cell ParentRow fast egendom. Returnerar cellens överordnade rad i C#.
type: docs
weight: 100
url: /sv/net/aspose.words.tables/cell/parentrow/
---
## Cell.ParentRow property

Returnerar cellens överordnade rad.

```csharp
public Row ParentRow { get; }
```

## Anmärkningar

Ekvivalent medFirstNonMarkupParentNode gjutna till[`Row`](../../row/).

## Exempel

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

* class [Row](../../row/)
* class [Cell](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
