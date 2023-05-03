---
title: PdfSaveOptions.ExportDocumentStructure
linktitle: ExportDocumentStructure
articleTitle: ExportDocumentStructure
second_title: Aspose.Words for .NET API Reference
description: PdfSaveOptions ExportDocumentStructure property. Gets or sets a value determining whether or not to export document structure in C#.
type: docs
weight: 140
url: /net/aspose.words.saving/pdfsaveoptions/exportdocumentstructure/
---
## PdfSaveOptions.ExportDocumentStructure property

Gets or sets a value determining whether or not to export document structure.

```csharp
public bool ExportDocumentStructure { get; set; }
```

## Remarks

This value is ignored when saving to PDF/A-1a, PDF/A-2a and PDF/UA-1 because document structure is required for this compliance.

Note that exporting the document structure significantly increases the memory consumption, especially for the large documents.

## Examples

Shows how to preserve document structure elements, which can assist in programmatically interpreting our document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Write(
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Set the "ExportDocumentStructure" property to "true" to make the document structure, such tags, available via the
// "Content" navigation pane of Adobe Acrobat at the cost of increased file size.
// Set the "ExportDocumentStructure" property to "false" to not export the document structure.
options.ExportDocumentStructure = exportDocumentStructure;

// Suppose we export document structure while saving this document. In that case,
// we can open it using Adobe Acrobat and find tags for elements such as the heading
// and the next paragraph via "View" -> "Show/Hide" -> "Navigation panes" -> "Tags".
doc.Save(ArtifactsDir + "PdfSaveOptions.ExportDocumentStructure.pdf", options);
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../pdfsaveoptions/)
* assembly [Aspose.Words](../../../)
