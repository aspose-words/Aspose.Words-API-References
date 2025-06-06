---
title: Cell.CellFormat
linktitle: CellFormat
articleTitle: CellFormat
second_title: Aspose.Words for .NET
description: Discover the Cell CellFormat property to easily access and customize cell formatting options for enhanced data presentation in your applications.
type: docs
weight: 20
url: /net/aspose.words.tables/cell/cellformat/
---
## Cell.CellFormat property

Provides access to the formatting properties of the cell.

```csharp
public CellFormat CellFormat { get; }
```

## Examples

Shows how to modify formatting of a table cell.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// Use a cell's "CellFormat" property to set formatting that modifies the appearance of that cell.
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
```

Shows how to combine the rows from two tables into one.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Below are two ways of getting a table from a document.
// 1 -  From the "Tables" collection of a Body node:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 -  Using the "GetChild" method:
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Append all rows from the current table to the next.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Remove the empty table container.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
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

* class [CellFormat](../../cellformat/)
* class [Cell](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
