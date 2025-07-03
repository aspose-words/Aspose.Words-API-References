---
title: Aspose::Words::Saving::PageSet::PageSet constructor
linktitle: PageSet
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PageSet::PageSet constructor. Creates a page set based on exact page indices in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.saving/pageset/pageset/
---
## PageSet::PageSet(const System::ArrayPtr\<int32_t\>\&) constructor


Creates a page set based on exact page indices.

```cpp
Aspose::Words::Saving::PageSet::PageSet(const System::ArrayPtr<int32_t> &pages)
```


| Parameter | Type | Description |
| --- | --- | --- |
| pages | const System::ArrayPtr\<int32_t\>\& | Zero-based indices of pages. |

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

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSet::PageSet(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) constructor


Creates a page set based on ranges.

```cpp
Aspose::Words::Saving::PageSet::PageSet(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Saving::PageRange>> &ranges)
```


| Parameter | Type | Description |
| --- | --- | --- |
| ranges | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\& | Array of page ranges. |

## Examples



Shows how to extract pages based on exact page ranges. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## See Also

* Class [PageRange](../../pagerange/)
* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSet::PageSet(int32_t) constructor


Creates an one-page set based on exact page index.

```cpp
Aspose::Words::Saving::PageSet::PageSet(int32_t page)
```


| Parameter | Type | Description |
| --- | --- | --- |
| page | int32_t | Zero-based index of the page. |

## Examples



Shows how to render one page from a document to a JPEG image. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Set the "PageSet" to "1" to select the second page via
// the zero-based index to start rendering the document from.
options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

// When we save the document to the JPEG format, Aspose.Words only renders one page.
// This image will contain one page starting from page two,
// which will just be the second page of the original document.
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.OnePage.jpg", options);
```

## See Also

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
