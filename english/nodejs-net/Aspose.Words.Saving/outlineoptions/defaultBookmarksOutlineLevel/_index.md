﻿---
title: OutlineOptions.defaultBookmarksOutlineLevel property
linktitle: defaultBookmarksOutlineLevel property
articleTitle: defaultBookmarksOutlineLevel property
second_title: Aspose.Words for Node.js
description: "OutlineOptions.defaultBookmarksOutlineLevel property. Specifies the default level in the document outline at which to display Word bookmarks."
type: docs
weight: 50
url: /nodejs-net/aspose.words.saving/outlineoptions/defaultBookmarksOutlineLevel/
---

## OutlineOptions.defaultBookmarksOutlineLevel property

Specifies the default level in the document outline at which to display Word bookmarks.


```js
get defaultBookmarksOutlineLevel(): number
```

### Remarks

Individual bookmarks level could be specified using [OutlineOptions.bookmarksOutlineLevels](../bookmarksOutlineLevels/) property.

Specify 0 and Word bookmarks will not be displayed in the document outline.
Specify 1 and Word bookmarks will be displayed in the document outline at level 1; 2 for level 2 and so on.

Default is 0. Valid range is 0 to 9.




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
* class [OutlineOptions](../)

