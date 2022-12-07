---
title: get_PageSet
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the pages to render. Default is all the pages in the document.
type: docs
weight: 105
url: /cpp/aspose.words.saving/fixedpagesaveoptions/get_pageset/
---
## FixedPageSaveOptions::get_PageSet method


Gets or sets the pages to render. Default is all the pages in the document.

```cpp
System::SharedPtr<Aspose::Words::Saving::PageSet> Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet() const
```


## Examples



Shows how to convert only some of the pages in a document to PDF. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page 3.");

{
    SharedPtr<System::IO::Stream> stream = System::IO::File::Create(ArtifactsDir + u"PdfSaveOptions.OnePage.pdf");
    // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
    // to modify how that method converts the document to .PDF.
    auto options = MakeObject<PdfSaveOptions>();

    // Set the "PageIndex" to "1" to render a portion of the document starting from the second page.
    options->set_PageSet(MakeObject<PageSet>(1));

    // This document will contain one page starting from page two, which will only contain the second page.
    doc->Save(stream, options);
}
```


Shows how to export Odd pages from the document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

for (int i = 0; i < 5; i++)
{
    builder->Writeln(String::Format(u"Page {0} ({1})", i + 1, (i % 2 == 0 ? String(u"odd") : String(u"even"))));
    if (i < 4)
    {
        builder->InsertBreak(BreakType::PageBreak);
    }
}

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// Below are three PageSet properties that we can use to filter out a set of pages from
// our document to save in an output PDF document based on the parity of their page numbers.
// 1 -  Save only the even-numbered pages:
options->set_PageSet(PageSet::get_Even());

doc->Save(ArtifactsDir + u"PdfSaveOptions.ExportPageSet.Even.pdf", options);

// 2 -  Save only the odd-numbered pages:
options->set_PageSet(PageSet::get_Odd());

doc->Save(ArtifactsDir + u"PdfSaveOptions.ExportPageSet.Odd.pdf", options);

// 3 -  Save every page:
options->set_PageSet(PageSet::get_All());

doc->Save(ArtifactsDir + u"PdfSaveOptions.ExportPageSet.All.pdf", options);
```


Shows how to extract pages based on exact page indices. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Add five pages to the document.
for (int i = 1; i < 6; i++)
{
    builder->Write(String(u"Page ") + i);
    builder->InsertBreak(BreakType::PageBreak);
}

// Create an "XpsSaveOptions" object, which we can pass to the document's "Save" method
// to modify how that method converts the document to .XPS.
auto xpsOptions = MakeObject<XpsSaveOptions>();

// Use the "PageSet" property to select a set of the document's pages to save to output XPS.
// In this case, we will choose, via a zero-based index, only three pages: page 1, page 2, and page 4.
xpsOptions->set_PageSet(MakeObject<PageSet>(MakeArray<int>({0, 1, 3})));

doc->Save(ArtifactsDir + u"XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

## See Also

* Class [PageSet](../../pageset/)
* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
