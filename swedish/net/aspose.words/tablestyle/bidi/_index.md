---
title: TableStyle.Bidi
second_title: Aspose.Words för .NET API Referens
description: TableStyle fast egendom. Hämtar eller ställer in om detta är en stil för en högertillvänstertabell.
type: docs
weight: 30
url: /sv/net/aspose.words/tablestyle/bidi/
---
## TableStyle.Bidi property

Hämtar eller ställer in om detta är en stil för en höger-till-vänster-tabell.

```csharp
public bool Bidi { get; set; }
```

### Anmärkningar

När`Sann`, är cellerna i rader utlagda från höger till vänster.

Standardvärdet är`falsk`.

### Exempel

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
* namnutrymme [Aspose.Words](../../tablestyle/)
* hopsättning [Aspose.Words](../../../)


