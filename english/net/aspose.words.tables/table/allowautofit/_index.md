---
title: Table.AllowAutoFit
linktitle: AllowAutoFit
articleTitle: AllowAutoFit
second_title: Aspose.Words for .NET
description: Discover the Table AllowAutoFit property to effortlessly resize Microsoft Word and Aspose.Words table cells, enhancing your document's readability and presentation.
type: docs
weight: 50
url: /net/aspose.words.tables/table/allowautofit/
---
## Table.AllowAutoFit property

Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents.

```csharp
public bool AllowAutoFit { get; set; }
```

## Remarks

The default value is `true`.

## Examples

Shows how to enable/disable automatic table cell resizing.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(100);
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.EndRow();
builder.EndTable();

// Set the "AllowAutoFit" property to "false" to get the table to maintain the dimensions
// of all its rows and cells, and truncate contents if they get too large to fit.
// Set the "AllowAutoFit" property to "true" to allow the table to change its cells' width and height
// to accommodate their contents.
table.AllowAutoFit = allowAutoFit;

doc.Save(ArtifactsDir + "Table.AllowAutoFitOnTable.html");
```

### See Also

* class [Table](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
