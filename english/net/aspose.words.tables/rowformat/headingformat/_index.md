---
title: RowFormat.HeadingFormat
linktitle: HeadingFormat
articleTitle: HeadingFormat
second_title: Aspose.Words for .NET
description: Discover the RowFormat HeadingFormat property, ensure your table headings repeat on every page for clarity and improved readability in multi-page documents.
type: docs
weight: 30
url: /net/aspose.words.tables/rowformat/headingformat/
---
## RowFormat.HeadingFormat property

True if the row is repeated as a table heading on every page when the table spans more than one page.

```csharp
public bool HeadingFormat { get; set; }
```

## Examples

Shows how to build a table with rows that repeat on every page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// Any rows inserted while the "HeadingFormat" flag is set to "true"
// will show up at the top of the table on every page that it spans.
builder.RowFormat.HeadingFormat = true;
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.CellFormat.Width = 100;
builder.InsertCell();
builder.Write("Heading row 1");
builder.EndRow();
builder.InsertCell();
builder.Write("Heading row 2");
builder.EndRow();

builder.CellFormat.Width = 50;
builder.ParagraphFormat.ClearFormatting();
builder.RowFormat.HeadingFormat = false;

// Add enough rows for the table to span two pages.
for (int i = 0; i < 50; i++)
{
    builder.InsertCell();
    builder.Write($"Row {table.Rows.Count}, column 1.");
    builder.InsertCell();
    builder.Write($"Row {table.Rows.Count}, column 2.");
    builder.EndRow();
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableSetHeadingRow.docx");
```

### See Also

* class [RowFormat](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
