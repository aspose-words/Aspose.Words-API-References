---
title: Aspose::Words::Saving::PageRange::PageRange constructor
linktitle: PageRange
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PageRange::PageRange constructor. Creates a new page range object in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.saving/pagerange/pagerange/
---
## PageRange::PageRange constructor


Creates a new page range object.

```cpp
Aspose::Words::Saving::PageRange::PageRange(int32_t from, int32_t to)
```


| Parameter | Type | Description |
| --- | --- | --- |
| from | int32_t | The starting page zero-based index. |
| to | int32_t | The ending page zero-based index. If it exceeds the index of the last page in the document, it is truncated to fit in the document on rendering. |

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

* Class [PageRange](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
