---
title: Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet method
linktitle: get_PageSet
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet method. Gets or sets the pages to render. Default is all the pages in the document in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.saving/fixedpagesaveoptions/get_pageset/
---
## FixedPageSaveOptions::get_PageSet method


Gets or sets the pages to render. Default is all the pages in the document.

```cpp
System::SharedPtr<Aspose::Words::Saving::PageSet> Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet() const
```


## Examples



Shows how to extract pages based on exact page indices. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Add five pages to the document.
for (int32_t i = 1; i < 6; i++)
{
    builder->Write(System::String(u"Page ") + i);
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Create an "XpsSaveOptions" object, which we can pass to the document's "Save" method
// to modify how that method converts the document to .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

// Use the "PageSet" property to select a set of the document's pages to save to output XPS.
// In this case, we will choose, via a zero-based index, only three pages: page 1, page 2, and page 4.
xpsOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<int32_t>({0, 1, 3})));

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

## See Also

* Class [PageSet](../../pageset/)
* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
