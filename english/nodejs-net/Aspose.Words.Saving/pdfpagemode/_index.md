---
title: PdfPageMode enumeration
linktitle: PdfPageMode enumeration
articleTitle: PdfPageMode enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.PdfPageMode enumeration. Specifies how the PDF document should be displayed when opened in the PDF reader."
type: docs
weight: 690
url: /nodejs-net/aspose.words.saving/pdfpagemode/
---

## PdfPageMode enumeration

Specifies how the PDF document should be displayed when opened in the PDF reader.


### Members

| Name | Description |
| --- | --- |
| UseNone | Neither document outline nor thumbnail images are visible. |
| UseOutlines | Document outline is visible. Note that if there're no outlines in the PDF document then outline navigation pane will not be visible anyway. |
| UseThumbs | Thumbnail images are visible. |
| FullScreen | Full-screen mode, with no menu bar, window controls, or any other window visible. |
| UseOC | Optional content group panel is visible. |
| UseAttachments | Attachments panel is visible. |

### Examples

Shows to process bookmarks in headers/footers in a document that we are rendering to PDF.

```js
let doc = new aw.Document(base.myDir + "Bookmarks in headers and footers.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let saveOptions = new aw.Saving.PdfSaveOptions();

// Set the "PageMode" property to "PdfPageMode.UseOutlines" to display the outline navigation pane in the output PDF.
saveOptions.pageMode = aw.Saving.PdfPageMode.UseOutlines;

// Set the "DefaultBookmarksOutlineLevel" property to "1" to display all
// bookmarks at the first level of the outline in the output PDF.
saveOptions.outlineOptions.defaultBookmarksOutlineLevel = 1;

// Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.None" to
// not export any bookmarks that are inside headers/footers.
// Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.First" to
// only export bookmarks in the first section's header/footers.
// Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.All" to
// export bookmarks that are in all headers/footers.
saveOptions.headerFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.save(base.artifactsDir + "PdfSaveOptions.headerFooterBookmarksExportMode.pdf", saveOptions);
```

Shows how to set instructions for some PDF readers to follow when opening an output document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world!");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

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
options.pageMode = pageMode;

doc.save(base.artifactsDir + "PdfSaveOptions.pageMode.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../)

