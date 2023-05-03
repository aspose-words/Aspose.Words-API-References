---
title: PdfSaveOptions.DisplayDocTitle
linktitle: DisplayDocTitle
second_title: Aspose.Words for .NET API Reference
description: PdfSaveOptions DisplayDocTitle property. A flag specifying whether the windows title bar should display the document title taken from the Title entry of the document information dictionary in C#.
type: docs
weight: 80
url: /net/aspose.words.saving/pdfsaveoptions/displaydoctitle/
---
## DisplayDocTitle property

A flag specifying whether the window’s title bar should display the document title taken from the Title entry of the document information dictionary.

```csharp
public bool DisplayDocTitle { get; set; }
```

## Remarks

If `false`, the title bar should instead display the name of the PDF file containing the document.

This flag is required by PDF/UA compliance. `true` value will be used automatically when saving to PDF/UA.

The default value is `false`.

## Examples

Shows how to display the title of the document as the title bar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.BuiltInDocumentProperties.Title = "Windows bar pdf title";

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
// Set the "DisplayDocTitle" to "true" to get some PDF readers, such as Adobe Acrobat Pro,
// to display the value of the document's "Title" built-in property in the tab that belongs to this document.
// Set the "DisplayDocTitle" to "false" to get such readers to display the document's filename.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { DisplayDocTitle = displayDocTitle };

doc.Save(ArtifactsDir + "PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../pdfsaveoptions/)
* assembly [Aspose.Words](../../../)
