---
title: Row.IsLastRow
second_title: Aspose.Words för .NET API Referens
description: Row fast egendom. Sant om detta är den sista raden i en tabell falskt annars.
type: docs
weight: 50
url: /sv/net/aspose.words.tables/row/islastrow/
---
## Row.IsLastRow property

Sant om detta är den sista raden i en tabell; falskt annars.

```csharp
public bool IsLastRow { get; }
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

* class [Row](../)
* namnutrymme [Aspose.Words.Tables](../../row/)
* hopsättning [Aspose.Words](../../../)


