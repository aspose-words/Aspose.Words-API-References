---
title: Row.RowFormat
second_title: Aspose.Words för .NET API Referens
description: Row fast egendom. Ger tillgång till formateringsegenskaperna för raden.
type: docs
weight: 110
url: /sv/net/aspose.words.tables/row/rowformat/
---
## Row.RowFormat property

Ger tillgång till formateringsegenskaperna för raden.

```csharp
public RowFormat RowFormat { get; }
```

### Exempel

Visar hur man ändrar formateringen av en tabellrad.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Använd den första radens "RowFormat"-egenskap för att ställa in formatering som ändrar hela radens utseende.
Row firstRow = table.FirstRow;
firstRow.RowFormat.Borders.LineStyle = LineStyle.None;
firstRow.RowFormat.HeightRule = HeightRule.Auto;
firstRow.RowFormat.AllowBreakAcrossPages = true;

doc.Save(ArtifactsDir + "Table.RowFormat.docx");
```

Visar hur du ändrar formatet för rader och celler i en tabell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("City");
builder.InsertCell();
builder.Write("Country");
builder.EndRow();
builder.InsertCell();
builder.Write("London");
builder.InsertCell();
builder.Write("U.K.");
builder.EndTable();

// Använd den första radens "RowFormat"-egenskap för att ändra formateringen
// av innehållet i alla celler i den här raden.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Använd egenskapen "CellFormat" för den första cellen i den sista raden för att ändra formateringen av cellens innehåll.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

### Se även

* class [RowFormat](../../rowformat/)
* class [Row](../)
* namnutrymme [Aspose.Words.Tables](../../row/)
* hopsättning [Aspose.Words](../../../)


