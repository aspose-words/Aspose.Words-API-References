---
title: "منشئ PageRange في Aspose::Words::Saving::PageRange."
linktitle: "PageRange"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ PageRange في Aspose::Words::Saving::PageRange. ينشئ كائن نطاق صفحات جديد في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.saving/pagerange/pagerange/
---
## PageRange::PageRange constructor


ينشئ كائن نطاق صفحة جديد.

```cpp
Aspose::Words::Saving::PageRange::PageRange(int32_t from, int32_t to)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| من | int32_t | فهرس الصفحة الابتدائية (مبني على الصفر). |
| إلى | int32_t | فهرس الصفحة النهائية (مبني على الصفر). إذا تجاوز فهرس الصفحة الأخيرة في المستند، يتم تقصيره ليتناسب مع المستند عند العرض. |

## أمثلة



يوضح كيفية استخراج الصفحات بناءً على نطاقات صفحات دقيقة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## انظر أيضًا

* Class [PageRange](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
