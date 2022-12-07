---
title: get_DefaultBookmarksOutlineLevel
second_title: Aspose.Words for C++ API Reference
description: Specifies the default level in the document outline at which to display Word bookmarks.
type: docs
weight: 66
url: /cpp/aspose.words.saving/outlineoptions/get_defaultbookmarksoutlinelevel/
---
## OutlineOptions::get_DefaultBookmarksOutlineLevel method


Specifies the default level in the document outline at which to display Word bookmarks.

```cpp
int32_t Aspose::Words::Saving::OutlineOptions::get_DefaultBookmarksOutlineLevel() const
```

## Remarks


Individual bookmarks level could be specified using [BookmarksOutlineLevels](../get_bookmarksoutlinelevels/) property.

Specify 0 and Word bookmarks will not be displayed in the document outline. Specify 1 and Word bookmarks will be displayed in the document outline at level 1; 2 for level 2 and so on.

Default is 0. Valid range is 0 to 9.

## Examples



Shows to process bookmarks in headers/footers in a document that we are rendering to PDF. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Bookmarks in headers and footers.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto saveOptions = MakeObject<PdfSaveOptions>();

// Set the "PageMode" property to "PdfPageMode.UseOutlines" to display the outline navigation pane in the output PDF.
saveOptions->set_PageMode(PdfPageMode::UseOutlines);

// Set the "DefaultBookmarksOutlineLevel" property to "1" to display all
// bookmarks at the first level of the outline in the output PDF.
saveOptions->get_OutlineOptions()->set_DefaultBookmarksOutlineLevel(1);

// Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.None" to
// not export any bookmarks that are inside headers/footers.
// Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.First" to
// only export bookmarks in the first section's header/footers.
// Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.All" to
// export bookmarks that are in all headers/footers.
saveOptions->set_HeaderFooterBookmarksExportMode(headerFooterBookmarksExportMode);

doc->Save(ArtifactsDir + u"PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

## See Also

* Class [OutlineOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
