---
title: get_DisplayDocTitle
second_title: Aspose.Words for C++ API Reference
description: A flag specifying whether the window’s title bar should display the document title taken from the Title entry of the document information dictionary.
type: docs
weight: 105
url: /cpp/aspose.words.saving/pdfsaveoptions/get_displaydoctitle/
---
## PdfSaveOptions.get_DisplayDocTitle method


A flag specifying whether the window’s title bar should display the document title taken from the Title entry of the document information dictionary.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_DisplayDocTitle() const
```


If **false**, the title bar should instead display the name of the PDF file containing the document.

This flag is required by PDF/UA compliance. **true** value will be used automatically when saving to PDF/UA.

The default value is **false**.

## Examples




Shows how to display the title of the document as the title bar. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->get_BuiltInDocumentProperties()->set_Title(u"Windows bar pdf title");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
// Set the "DisplayDocTitle" to "true" to get some PDF readers, such as Adobe Acrobat Pro,
// to display the value of the document's "Title" built-in property in the tab that belongs to this document.
// Set the "DisplayDocTitle" to "false" to get such readers to display the document's filename.
auto pdfSaveOptions = MakeObject<PdfSaveOptions>();
pdfSaveOptions->set_DisplayDocTitle(displayDocTitle);

doc->Save(ArtifactsDir + u"PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

