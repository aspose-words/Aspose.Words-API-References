---
title: PageRange
second_title: Aspose.Words for C++ API Reference
description: Creates a new page range object.
type: docs
weight: 1
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
auto doc = MakeObject<Document>(MyDir + u"Images.docx");

auto imageOptions = MakeObject<ImageSaveOptions>(SaveFormat::Tiff);
auto pageSet = MakeObject<PageSet>(MakeArray<SharedPtr<PageRange>>(
    {MakeObject<PageRange>(1, 1), MakeObject<PageRange>(2, 3), MakeObject<PageRange>(1, 3), MakeObject<PageRange>(2, 4), MakeObject<PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(ArtifactsDir + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## See Also

* Class [PageRange](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
