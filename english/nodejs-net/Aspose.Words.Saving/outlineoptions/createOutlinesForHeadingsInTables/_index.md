---
title: OutlineOptions.createOutlinesForHeadingsInTables property
linktitle: createOutlinesForHeadingsInTables property
articleTitle: createOutlinesForHeadingsInTables property
second_title: Aspose.Words for NodeJs
description: "OutlineOptions.createOutlinesForHeadingsInTables property. Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Saving/outlineoptions/createOutlinesForHeadingsInTables/
---

## OutlineOptions.createOutlinesForHeadingsInTables property

Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables.


```js
get createOutlinesForHeadingsInTables(): boolean
```

### Remarks

Default value is ``False``.




### Examples

Shows how to create PDF document outline entries for headings inside tables.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Create a table with three rows. The first row,
// whose text we will format in a heading-type style, will serve as the column header.
builder.startTable();
builder.insertCell();
builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading1;
builder.write("Customers");
builder.endRow();
builder.insertCell();
builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Normal;
builder.write("John Doe");
builder.endRow();
builder.insertCell();
builder.write("Jane Doe");
builder.endTable();

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let pdfSaveOptions = new aw.Saving.PdfSaveOptions();

// The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
// Clicking on an entry in this outline will take us to the location of its respective heading.
// Set the "HeadingsOutlineLevels" property to "1" to get the outline
// to only register headings with heading levels that are no larger than 1.
pdfSaveOptions.outlineOptions.headingsOutlineLevels = 1;

// Set the "CreateOutlinesForHeadingsInTables" property to "false" to exclude all headings within tables,
// such as the one we have created above from the outline.
// Set the "CreateOutlinesForHeadingsInTables" property to "true" to include all headings within tables
// in the outline, provided that they have a heading level that is no larger than the value of the "HeadingsOutlineLevels" property.
pdfSaveOptions.outlineOptions.createOutlinesForHeadingsInTables = createOutlinesForHeadingsInTables;

doc.save(base.artifactsDir + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [OutlineOptions](../)

