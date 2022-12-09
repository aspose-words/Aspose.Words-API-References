---
title: PageSet
second_title: Aspose.Words for C++ API Reference
description: Creates a page set based on exact page indices.
type: docs
weight: 53
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

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
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
auto doc = MakeObject<Document>(MyDir + u"Images.docx");

auto imageOptions = MakeObject<ImageSaveOptions>(SaveFormat::Tiff);
auto pageSet = MakeObject<PageSet>(MakeArray<SharedPtr<PageRange>>(
    {MakeObject<PageRange>(1, 1), MakeObject<PageRange>(2, 3), MakeObject<PageRange>(1, 3), MakeObject<PageRange>(2, 4), MakeObject<PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(ArtifactsDir + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## See Also

* Class [PageRange](../../pagerange/)
* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
## PageSet::PageSet(int32_t) constructor


Creates an one-page set based on exact page index.

```cpp
Aspose::Words::Saving::PageSet::PageSet(int32_t page)
```


| Parameter | Type | Description |
| --- | --- | --- |
| page | int32_t | Zero-based index of the page. |

## See Also

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
