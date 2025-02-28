---
title: CellFormat.PreferredWidth
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words for .NET
description: Discover the CellFormat PreferredWidth property to easily customize cell widths for optimal layout and design in your spreadsheets. Enhance your data presentation!
type: docs
weight: 80
url: /net/aspose.words.tables/cellformat/preferredwidth/
---
## CellFormat.PreferredWidth property

Returns or sets the preferred width of the cell.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

## Remarks

The preferred width (along with the table's Auto Fit option) determines how the actual width of the cell is calculated by the table layout algorithm. Table layout can be performed by Aspose.Words when it saves the document or by Microsoft Word when it displays the document.

The preferred width can be specified in points or in percent. The preferred width can also be specified as "auto", which means no preferred width is specified.

The default value is [`Auto`](../../preferredwidth/auto/).

## Examples

Shows how to set a preferred width for table cells.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// There are two ways of applying the "PreferredWidth" class to table cells.
// 1 -  Set an absolute preferred width based on points:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 -  Set a relative preferred width based on percent of the table's width:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// A cell with no preferred width specified will take up the rest of the available space.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// Each configuration of the "PreferredWidth" property creates a new object.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### See Also

* class [PreferredWidth](../../preferredwidth/)
* class [CellFormat](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
