---
title: Cell.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Cell LastParagraph. Få enkel åtkomst till det sista stycket från direkta underordnade element för effektiv innehållshantering.
type: docs
weight: 60
url: /sv/net/aspose.words.tables/cell/lastparagraph/
---
## Cell.LastParagraph property

Hämtar det sista stycket bland de omedelbara underordnade.

```csharp
public Paragraph LastParagraph { get; }
```

## Exempel

Visar hur man tillämpar inställningar på vertikala kantlinjer i en tabellrads format.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa en tabell med röda och blå innerkanter.
Table table = builder.StartTable();

for (int i = 0; i < 3; i++)
{
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 1");
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 2");

    Row row = builder.EndRow();
    BorderCollection borders = row.RowFormat.Borders;

    // Justera utseendet på kantlinjer som ska visas mellan rader.
    borders.Horizontal.Color = Color.Red;
    borders.Horizontal.LineStyle = LineStyle.Dot;
    borders.Horizontal.LineWidth = 2.0d;

    // Justera utseendet på kantlinjer som ska visas mellan celler.
    borders.Vertical.Color = Color.Blue;
    borders.Vertical.LineStyle = LineStyle.Dot;
    borders.Vertical.LineWidth = 2.0d;
}

// Ett radformat och ett cells inre stycke använder olika kantlinjer.
Border border = table.FirstRow.FirstCell.LastParagraph.ParagraphFormat.Borders.Vertical;

Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
Assert.AreEqual(0.0d, border.LineWidth);
Assert.AreEqual(LineStyle.None, border.LineStyle);

doc.Save(ArtifactsDir + "Border.VerticalBorders.docx");
```

### Se även

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Cell](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
