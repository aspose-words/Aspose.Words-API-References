---
title: TableStyle.TopPadding
linktitle: TopPadding
articleTitle: TopPadding
second_title: Aspose.Words för .NET
description: TableStyle TopPadding fast egendom. Hämtar eller ställer in mängden utrymme i poäng som ska läggas till ovanför innehållet i tabellceller i C#.
type: docs
weight: 140
url: /sv/net/aspose.words/tablestyle/toppadding/
---
## TableStyle.TopPadding property

Hämtar eller ställer in mängden utrymme (i poäng) som ska läggas till ovanför innehållet i tabellceller.

```csharp
public double TopPadding { get; set; }
```

## Exempel

Visar hur man skapar anpassade stilinställningar för tabellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// Att ställa in stilegenskaperna för en tabell kan påverka egenskaperna för själva tabellen.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### Se även

* class [TableStyle](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
