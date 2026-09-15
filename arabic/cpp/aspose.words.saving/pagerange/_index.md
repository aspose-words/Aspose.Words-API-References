---
title: "فئة Aspose::Words::Saving::PageRange"
linktitle: "PageRange"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Saving::PageRange. تمثّل نطاقًا مستمرًا من الصفحات. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 18000
url: /ar/cpp/aspose.words.saving/pagerange/
---
## PageRange class


يمثل نطاقًا مستمرًا من الصفحات. لمعرفة المزيد، زر مقالة الوثائق [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class PageRange : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageRange](./pagerange/)(int32_t, int32_t) | ينشئ كائن نطاق صفحة جديد. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
