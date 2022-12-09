---
title: get_ExportDocumentStructure
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining whether or not to export document structure.
type: docs
weight: 196
url: /cpp/aspose.words.saving/pdfsaveoptions/get_exportdocumentstructure/
---
## PdfSaveOptions::get_ExportDocumentStructure method


Gets or sets a value determining whether or not to export document structure.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportDocumentStructure() const
```

## Remarks


This value is ignored when saving to PDF/A-1a, PDF/A-2a and PDF/UA-1 because document structure is required for this compliance.

Note that exporting the document structure significantly increases the memory consumption, especially for the large documents.

## Examples



Shows how to preserve document structure elements, which can assist in programmatically interpreting our document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// Set the "ExportDocumentStructure" property to "true" to make the document structure, such tags, available via the
// "Content" navigation pane of Adobe Acrobat at the cost of increased file size.
// Set the "ExportDocumentStructure" property to "false" to not export the document structure.
options->set_ExportDocumentStructure(exportDocumentStructure);

// Suppose we export document structure while saving this document. In that case,
// we can open it using Adobe Acrobat and find tags for elements such as the heading
// and the next paragraph via "View" -> "Show/Hide" -> "Navigation panes" -> "Tags".
doc->Save(ArtifactsDir + u"PdfSaveOptions.ExportDocumentStructure.pdf", options);
```

## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
