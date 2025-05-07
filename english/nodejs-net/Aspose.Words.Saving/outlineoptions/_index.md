---
title: OutlineOptions class
linktitle: OutlineOptions class
articleTitle: OutlineOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.OutlineOptions class. Allows to specify outline options"
type: docs
weight: 530
url: /nodejs-net/aspose.words.saving/outlineoptions/
---

## OutlineOptions class

Allows to specify outline options.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/nodejs-net/save-a-document/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [OutlineOptions()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmarksOutlineLevels](./bookmarksOutlineLevels/) | Allows to specify individual bookmarks outline level. |
| [createMissingOutlineLevels](./createMissingOutlineLevels/) | Gets or sets a value determining whether or not to create missing outline levels when the document is  exported. |
| [createOutlinesForHeadingsInTables](./createOutlinesForHeadingsInTables/) | Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables. |
| [defaultBookmarksOutlineLevel](./defaultBookmarksOutlineLevel/) | Specifies the default level in the document outline at which to display Word bookmarks. |
| [expandedOutlineLevels](./expandedOutlineLevels/) | Specifies how many levels in the document outline to show expanded when the file is viewed. |
| [headingsOutlineLevels](./headingsOutlineLevels/) | Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the  document outline. |

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

