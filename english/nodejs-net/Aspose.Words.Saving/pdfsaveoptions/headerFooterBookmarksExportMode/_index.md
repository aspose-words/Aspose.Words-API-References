---
title: PdfSaveOptions.headerFooterBookmarksExportMode property
linktitle: headerFooterBookmarksExportMode property
articleTitle: headerFooterBookmarksExportMode property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.headerFooterBookmarksExportMode property. Determines how bookmarks in headers/footers are exported."
type: docs
weight: 180
url: /nodejs-net/Aspose.Words.Saving/pdfsaveoptions/headerFooterBookmarksExportMode/
---

## PdfSaveOptions.headerFooterBookmarksExportMode property

Determines how bookmarks in headers/footers are exported.


```js
get headerFooterBookmarksExportMode(): Aspose.Words.Saving.HeaderFooterBookmarksExportMode
```

### Remarks

The default value is [HeaderFooterBookmarksExportMode.All](../../headerfooterbookmarksexportmode/#All).

This property is used in conjunction with the [PdfSaveOptions.outlineOptions](../outlineOptions/) option.




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

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

