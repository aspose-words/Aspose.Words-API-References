---
title: Aspose::Words::Saving::PdfSaveOptions::get_PageMode method
linktitle: get_PageMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::get_PageMode method. Specifies how the PDF document should be displayed when opened in the PDF reader in C++.'
type: docs
weight: 26000
url: /cpp/aspose.words.saving/pdfsaveoptions/get_pagemode/
---
## PdfSaveOptions::get_PageMode method


Specifies how the PDF document should be displayed when opened in the PDF reader.

```cpp
Aspose::Words::Saving::PdfPageMode Aspose::Words::Saving::PdfSaveOptions::get_PageMode() const
```


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


Shows how to set instructions for some PDF readers to follow when opening an output document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// Set the "PageMode" property to "PdfPageMode.FullScreen" to get the PDF reader to open the saved
// document in full-screen mode, which takes over the monitor's display and has no controls visible.
// Set the "PageMode" property to "PdfPageMode.UseThumbs" to get the PDF reader to display a separate panel
// with a thumbnail for each page in the document.
// Set the "PageMode" property to "PdfPageMode.UseOC" to get the PDF reader to display a separate panel
// that allows us to work with any layers present in the document.
// Set the "PageMode" property to "PdfPageMode.UseOutlines" to get the PDF reader
// also to display the outline, if possible.
// Set the "PageMode" property to "PdfPageMode.UseNone" to get the PDF reader to display just the document itself.
options->set_PageMode(pageMode);

doc->Save(ArtifactsDir + u"PdfSaveOptions.PageMode.pdf", options);
```

## See Also

* Enum [PdfPageMode](../../pdfpagemode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
