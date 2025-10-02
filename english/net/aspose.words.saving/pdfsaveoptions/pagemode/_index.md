---
title: PdfSaveOptions.PageMode
linktitle: PageMode
articleTitle: PageMode
second_title: Aspose.Words for .NET
description: Discover how the PdfSaveOptions PageMode property enhances your PDF viewing experience by customizing document display in any PDF reader.
type: docs
weight: 270
url: /net/aspose.words.saving/pdfsaveoptions/pagemode/
---
## PdfSaveOptions.PageMode property

Specifies how the PDF document should be displayed when opened in a PDF reader.

```csharp
public PdfPageMode PageMode { get; set; }
```

## Remarks

The default value is UseOutlines.

## Examples

Shows how to set instructions for some PDF readers to follow when opening an output document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Set the "PageMode" property to "PdfPageMode.FullScreen" to get the PDF reader to open the saved
// document in full-screen mode, which takes over the monitor's display and has no controls visible.
// Set the "PageMode" property to "PdfPageMode.UseThumbs" to get the PDF reader to display a separate panel
// with a thumbnail for each page in the document.
// Set the "PageMode" property to "PdfPageMode.UseOC" to get the PDF reader to display a separate panel
// that allows us to work with any layers present in the document.
// Set the "PageMode" property to "PdfPageMode.UseOutlines" to get the PDF reader
// also to display the outline, if possible.
// Set the "PageMode" property to "PdfPageMode.UseNone" to get the PDF reader to display just the document itself.
// Set the "PageMode" property to "PdfPageMode.UseAttachments" to make visible attachments panel.
options.PageMode = pageMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageMode.pdf", options);
```

Shows to process bookmarks in headers/footers in a document that we are rendering to PDF.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Set the "PageMode" property to "PdfPageMode.UseOutlines" to display the outline navigation pane in the output PDF.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Set the "DefaultBookmarksOutlineLevel" property to "1" to display all
// bookmarks at the first level of the outline in the output PDF.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.None" to
// not export any bookmarks that are inside headers/footers.
// Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.First" to
// only export bookmarks in the first section's header/footers.
// Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.All" to
// export bookmarks that are in all headers/footers.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### See Also

* enum [PdfPageMode](../../pdfpagemode/)
* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
