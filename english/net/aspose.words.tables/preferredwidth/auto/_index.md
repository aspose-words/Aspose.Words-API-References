---
title: PreferredWidth.Auto
linktitle: Auto
articleTitle: Auto
second_title: Aspose.Words for .NET
description: PreferredWidth Auto field. Returns an instance that represents the preferred width is not specified value in C#.
type: docs
weight: 10
url: /net/aspose.words.tables/preferredwidth/auto/
---
## PreferredWidth.Auto field

Returns an instance that represents the "preferred width is not specified" value.

```csharp
public static readonly PreferredWidth Auto;
```

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

* class [PreferredWidth](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
