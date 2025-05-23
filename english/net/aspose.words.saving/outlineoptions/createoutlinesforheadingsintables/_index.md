---
title: OutlineOptions.CreateOutlinesForHeadingsInTables
linktitle: CreateOutlinesForHeadingsInTables
articleTitle: CreateOutlinesForHeadingsInTables
second_title: Aspose.Words for .NET
description: Discover how the CreateOutlinesForHeadingsInTables property enhances table organization by enabling outlines for heading styles, improving document clarity.
type: docs
weight: 40
url: /net/aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/
---
## OutlineOptions.CreateOutlinesForHeadingsInTables property

Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables.

```csharp
public bool CreateOutlinesForHeadingsInTables { get; set; }
```

## Remarks

Default value is `false`.

## Examples

Shows how to create PDF document outline entries for headings inside tables.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a table with three rows. The first row,
// whose text we will format in a heading-type style, will serve as the column header.
builder.StartTable();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("Customers");
builder.EndRow();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Write("John Doe");
builder.EndRow();
builder.InsertCell();
builder.Write("Jane Doe");
builder.EndTable();

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
// Clicking on an entry in this outline will take us to the location of its respective heading.
// Set the "HeadingsOutlineLevels" property to "1" to get the outline
// to only register headings with heading levels that are no larger than 1.
pdfSaveOptions.OutlineOptions.HeadingsOutlineLevels = 1;

// Set the "CreateOutlinesForHeadingsInTables" property to "false" to exclude all headings within tables,
// such as the one we have created above from the outline.
// Set the "CreateOutlinesForHeadingsInTables" property to "true" to include all headings within tables
// in the outline, provided that they have a heading level that is no larger than the value of the "HeadingsOutlineLevels" property.
pdfSaveOptions.OutlineOptions.CreateOutlinesForHeadingsInTables = createOutlinesForHeadingsInTables;

doc.Save(ArtifactsDir + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
```

### See Also

* class [OutlineOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
