---
title: Table.AutoFit
linktitle: AutoFit
articleTitle: AutoFit
second_title: Aspose.Words for .NET API Reference
description: Table AutoFit method. Resizes the table and cells according to the specified auto fit behavior in C#.
type: docs
weight: 360
url: /net/aspose.words.tables/table/autofit/
---
## Table.AutoFit method

Resizes the table and cells according to the specified auto fit behavior.

```csharp
public void AutoFit(AutoFitBehavior behavior)
```

| Parameter | Type | Description |
| --- | --- | --- |
| behavior | AutoFitBehavior | Specifies how to auto fit the table. |

## Remarks

This method mimics the commands available in the Auto Fit menu for a table in Microsoft Word. The commands available are "Auto Fit to Contents", "Auto Fit to Window" and "Fixed Column Width". In Microsoft Word these commands set relevant table properties and then update the table layout and Aspose.Words does the same for you.

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

* enum [AutoFitBehavior](../../autofitbehavior/)
* class [Table](../)
* namespace [Aspose.Words.Tables](../../table/)
* assembly [Aspose.Words](../../../)
