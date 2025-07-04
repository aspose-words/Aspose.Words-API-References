---
title: Row.RowFormat
linktitle: RowFormat
articleTitle: RowFormat
second_title: Aspose.Words for .NET
description: Discover the Row RowFormat property for easy access to customizable row formatting options, enhancing your data presentation effortlessly.
type: docs
weight: 120
url: /net/aspose.words.tables/row/rowformat/
---
## Row.RowFormat property

Provides access to the formatting properties of the row.

```csharp
public RowFormat RowFormat { get; }
```

## Examples

Shows how to modify formatting of a table row.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Use the first row's "RowFormat" property to set formatting that modifies that entire row's appearance.
Row firstRow = table.FirstRow;
firstRow.RowFormat.Borders.LineStyle = LineStyle.None;
firstRow.RowFormat.HeightRule = HeightRule.Auto;
firstRow.RowFormat.AllowBreakAcrossPages = true;

doc.Save(ArtifactsDir + "Table.RowFormat.docx");
```

Shows how to modify the format of rows and cells in a table.

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

// Use the first row's "RowFormat" property to modify the formatting
// of the contents of all cells in this row.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Use the "CellFormat" property of the first cell in the last row to modify the formatting of that cell's contents.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

### See Also

* class [RowFormat](../../rowformat/)
* class [Row](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
