---
title: TableStyle.LeftIndent
linktitle: LeftIndent
articleTitle: LeftIndent
second_title: Aspose.Words för .NET
description: Upptäck egenskapen TableStyle LeftIndent för att enkelt anpassa tabellens vänstra indrag för förbättrad layoutkontroll och visuell tilltal.
type: docs
weight: 90
url: /sv/net/aspose.words/tablestyle/leftindent/
---
## TableStyle.LeftIndent property

Hämtar eller anger värdet som representerar den vänstra indragningen i en tabell.

```csharp
public double LeftIndent { get; set; }
```

## Exempel

Visar hur man ställer in en tabells position.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan följer två sätt att justera en tabell horisontellt.
// 1 - Använd egenskapen "Justering" för att justera den till en plats på sidan, till exempel mitten:
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Alignment = TableAlignment.Center;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.Single;

// Infoga en tabell och använd den stil vi skapade på den.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned to the center of the page");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

// 2 - Använd "LeftIndent" för att ange ett indrag från sidans vänstra marginal:
tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle2");
tableStyle.LeftIndent = 55;
tableStyle.Borders.Color = Color.Green;
tableStyle.Borders.LineStyle = LineStyle.Single;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned according to left indent");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

doc.Save(ArtifactsDir + "Table.SetTableAlignment.docx");
```

### Se även

* class [TableStyle](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
