---
title: DocumentBuilder.ParagraphFormat
linktitle: ParagraphFormat
articleTitle: ParagraphFormat
second_title: Aspose.Words for .NET
description: Explore the DocumentBuilder's ParagraphFormat property to access and customize essential paragraph formatting features for enhanced document styling.
type: docs
weight: 170
url: /net/aspose.words/documentbuilder/paragraphformat/
---
## DocumentBuilder.ParagraphFormat property

Returns an object that represents current paragraph formatting properties.

```csharp
public ParagraphFormat ParagraphFormat { get; }
```

## Examples

Shows how to create a formatted table using DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
table.LeftIndent = 20;

// Set some formatting options for text and table appearance.
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// Configuring the formatting options in a document builder will apply them
// to the current cell/row its cursor is in,
// as well as any new cells and rows created using that builder.
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// Reconfigure the builder's formatting objects for new rows and cells that we are about to make.
// The builder will not apply these to the first row already created so that it will stand out as a header row.
builder.CellFormat.Shading.BackgroundPatternColor = Color.White;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.RowFormat.Height = 30;
builder.RowFormat.HeightRule = HeightRule.Auto;
builder.InsertCell();
builder.Font.Size = 12;
builder.Font.Bold = false;

builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");
builder.InsertCell();
builder.Write("Row 1, Cell 3.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.InsertCell();
builder.Write("Row 2, Cell 3.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateFormattedTable.docx");
```

### See Also

* class [ParagraphFormat](../../paragraphformat/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
