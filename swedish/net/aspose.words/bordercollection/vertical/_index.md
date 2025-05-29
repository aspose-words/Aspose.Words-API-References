---
title: BorderCollection.Vertical
linktitle: Vertical
articleTitle: Vertical
second_title: Aspose.Words för .NET
description: Upptäck egenskapen BorderCollection Vertical för sömlösa cellkanter. Förbättra din design med anpassningsbara vertikala kantlinjer för ett elegant utseende!
type: docs
weight: 130
url: /sv/net/aspose.words/bordercollection/vertical/
---
## BorderCollection.Vertical property

Hämtar den vertikala kantlinjen som används mellan celler.

```csharp
public Border Vertical { get; }
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

* class [Border](../../border/)
* class [BorderCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
