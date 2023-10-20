---
title: BorderCollection.Horizontal
linktitle: Horizontal
articleTitle: Horizontal
second_title: Aspose.Words för .NET
description: BorderCollection Horizontal fast egendom. Hämtar den horisontella ram som används mellan celler eller överensstämmande stycken i C#.
type: docs
weight: 50
url: /sv/net/aspose.words/bordercollection/horizontal/
---
## BorderCollection.Horizontal property

Hämtar den horisontella ram som används mellan celler eller överensstämmande stycken.

```csharp
public Border Horizontal { get; }
```

## Exempel

Visar hur man tillämpar inställningar på horisontella ramar på ett styckes format.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa en röd horisontell ram för stycket. Alla stycken som skapas efteråt kommer att ärva dessa raminställningar.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
borders.Horizontal.Color = Color.Red;
borders.Horizontal.LineStyle = LineStyle.DashSmallGap;
borders.Horizontal.LineWidth = 3;

// Skriv text till dokumentet utan att skapa ett nytt stycke efteråt.
// Eftersom det inte finns något stycke under, kommer den horisontella gränsen inte att vara synlig.
builder.Write("Paragraph above horizontal border.");

// När vi lägger till ett andra stycke, kommer gränsen för det första stycket att bli synlig.
builder.InsertParagraph();
builder.Write("Paragraph below horizontal border.");

doc.Save(ArtifactsDir + "Border.HorizontalBorders.docx");
```

Visar hur man tillämpar inställningar på vertikala ramar på en tabellrads format.

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

    // Justera utseendet på kanter som kommer att visas mellan rader.
    borders.Horizontal.Color = Color.Red;
    borders.Horizontal.LineStyle = LineStyle.Dot;
    borders.Horizontal.LineWidth = 2.0d;

    // Justera utseendet på kanter som kommer att visas mellan celler.
    borders.Vertical.Color = Color.Blue;
    borders.Vertical.LineStyle = LineStyle.Dot;
    borders.Vertical.LineWidth = 2.0d;
}

// Ett radformat och en cells inre stycke använder olika raminställningar.
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
