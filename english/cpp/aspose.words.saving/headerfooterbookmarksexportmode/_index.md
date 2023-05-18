---
title: Aspose::Words::Saving::HeaderFooterBookmarksExportMode enum
linktitle: HeaderFooterBookmarksExportMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HeaderFooterBookmarksExportMode enum. Specifies how bookmarks in headers/footers are exported in C++.'
type: docs
weight: 57000
url: /cpp/aspose.words.saving/headerfooterbookmarksexportmode/
---
## HeaderFooterBookmarksExportMode enum


Specifies how bookmarks in headers/footers are exported.

```cpp
enum class HeaderFooterBookmarksExportMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | Bookmarks in headers/footers are not exported. |
| First | 1 | Only bookmark in first header/footer of the section is exported. |
| All | 2 | Bookmarks in all headers/footers are exported. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
