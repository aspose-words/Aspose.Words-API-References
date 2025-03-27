---
title: HeaderFooterBookmarksExportMode enumeration
linktitle: HeaderFooterBookmarksExportMode enumeration
articleTitle: HeaderFooterBookmarksExportMode enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.HeaderFooterBookmarksExportMode enumeration. Specifies how bookmarks in headers/footers are exported."
type: docs
weight: 210
url: /nodejs-net/Aspose.Words.Saving/headerfooterbookmarksexportmode/
---

## HeaderFooterBookmarksExportMode enumeration

Specifies how bookmarks in headers/footers are exported.


### Members

| Name | Description |
| --- | --- |
| None | Bookmarks in headers/footers are not exported. |
| First | Only bookmark in first header/footer of the section is exported. |
| All | Bookmarks in all headers/footers are exported. |

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

### See Also

* module [Aspose.Words.Saving](../)

