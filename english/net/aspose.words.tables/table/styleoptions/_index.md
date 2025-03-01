---
title: Table.StyleOptions
linktitle: StyleOptions
articleTitle: StyleOptions
second_title: Aspose.Words for .NET
description: Discover the Table StyleOptions property to customize your table's appearance with flexible bit flags. Enhance your table's style effortlessly!
type: docs
weight: 300
url: /net/aspose.words.tables/table/styleoptions/
---
## Table.StyleOptions property

Gets or sets bit flags that specify how a table style is applied to this table.

```csharp
public TableStyleOptions StyleOptions { get; set; }
```

## Examples

Shows how to build a new table while applying a style.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// We must insert at least one row before setting any table formatting.
builder.InsertCell();

// Set the table style used based on the style identifier.
// Note that not all table styles are available when saving to .doc format.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Partially apply the style to features of the table based on predicates, then build the table.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

### See Also

* enum [TableStyleOptions](../../tablestyleoptions/)
* class [Table](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
