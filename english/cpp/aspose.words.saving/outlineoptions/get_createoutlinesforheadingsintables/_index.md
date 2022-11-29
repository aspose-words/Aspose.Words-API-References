---
title: get_CreateOutlinesForHeadingsInTables
second_title: Aspose.Words for C++ API Reference
description: Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables.
type: docs
weight: 40
url: /cpp/aspose.words.saving/outlineoptions/get_createoutlinesforheadingsintables/
---
## OutlineOptions::get_CreateOutlinesForHeadingsInTables method


Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables.

```cpp
bool Aspose::Words::Saving::OutlineOptions::get_CreateOutlinesForHeadingsInTables() const
```

## Remarks


Default value is **false**.

## Examples



Shows how to create PDF document outline entries for headings inside tables. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create a table with three rows. The first row,
// whose text we will format in a heading-type style, will serve as the column header.
builder->StartTable();
builder->InsertCell();
builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading1);
builder->Write(u"Customers");
builder->EndRow();
builder->InsertCell();
builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Normal);
builder->Write(u"John Doe");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Jane Doe");
builder->EndTable();

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto pdfSaveOptions = MakeObject<PdfSaveOptions>();

// The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
// Clicking on an entry in this outline will take us to the location of its respective heading.
// Set the "HeadingsOutlineLevels" property to "1" to get the outline
// to only register headings with heading levels that are no larger than 1.
pdfSaveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(1);

// Set the "CreateOutlinesForHeadingsInTables" property to "false" to exclude all headings within tables,
// such as the one we have created above from the outline.
// Set the "CreateOutlinesForHeadingsInTables" property to "true" to include all headings within tables
// in the outline, provided that they have a heading level that is no larger than the value of the "HeadingsOutlineLevels" property.
pdfSaveOptions->get_OutlineOptions()->set_CreateOutlinesForHeadingsInTables(createOutlinesForHeadingsInTables);

doc->Save(ArtifactsDir + u"PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
```

## See Also

* Class [OutlineOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
