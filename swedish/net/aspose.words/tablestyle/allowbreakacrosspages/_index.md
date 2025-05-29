---
title: TableStyle.AllowBreakAcrossPages
linktitle: AllowBreakAcrossPages
articleTitle: AllowBreakAcrossPages
second_title: Aspose.Words för .NET
description: Upptäck egenskapen TableStyle AllowBreakAcrossPages, styr textflödet i tabeller och förbättra dokumentets läsbarhet över olika sidor.
type: docs
weight: 20
url: /sv/net/aspose.words/tablestyle/allowbreakacrosspages/
---
## TableStyle.AllowBreakAcrossPages property

Hämtar eller ställer in en flagga som anger om text i en tabellrad får delas över en sidbrytning.

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

## Anmärkningar

Standardvärdet är`sann` .

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
