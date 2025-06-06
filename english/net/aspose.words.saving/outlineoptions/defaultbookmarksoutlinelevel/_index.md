---
title: OutlineOptions.DefaultBookmarksOutlineLevel
linktitle: DefaultBookmarksOutlineLevel
articleTitle: DefaultBookmarksOutlineLevel
second_title: Aspose.Words for .NET
description: Discover how the DefaultBookmarksOutlineLevel property enhances your Word documents by optimizing bookmark visibility in the outline. Boost productivity today!
type: docs
weight: 50
url: /net/aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/
---
## OutlineOptions.DefaultBookmarksOutlineLevel property

Specifies the default level in the document outline at which to display Word bookmarks.

```csharp
public int DefaultBookmarksOutlineLevel { get; set; }
```

## Remarks

Individual bookmarks level could be specified using [`BookmarksOutlineLevels`](../bookmarksoutlinelevels/) property.

Specify 0 and Word bookmarks will not be displayed in the document outline. Specify 1 and Word bookmarks will be displayed in the document outline at level 1; 2 for level 2 and so on.

Default is 0. Valid range is 0 to 9.

## Examples

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

* class [OutlineOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
