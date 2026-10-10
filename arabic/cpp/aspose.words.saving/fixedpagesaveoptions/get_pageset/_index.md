---
title: "طريقة Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet"
linktitle: "get_PageSet"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet. يحصل على أو يحدد الصفحات التي سيتم عرضها. القيمة الافتراضية هي جميع الصفحات في المستند في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.saving/fixedpagesaveoptions/get_pageset/
---
## FixedPageSaveOptions::get_PageSet method


يحصل أو يضبط الصفحات التي سيتم عرضها. القيمة الافتراضية هي جميع الصفحات في المستند.

```cpp
System::SharedPtr<Aspose::Words::Saving::PageSet> Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet() const
```


## أمثلة



يوضح كيفية استخراج الصفحات بناءً على مؤشرات الصفحات الدقيقة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أضف خمس صفحات إلى المستند.
for (int32_t i = 1; i < 6; i++)
{
    builder->Write(System::String(u"Page ") + i);
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// أنشئ كائن "XpsSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل تلك الطريقة للمستند إلى .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

// استخدم الخاصية "PageSet" لتحديد مجموعة من صفحات المستند لحفظها في XPS الناتج.
// في هذه الحالة، سنختار، عبر فهرس يبدأ من الصفر، ثلاث صفحات فقط: الصفحة 1، الصفحة 2، والصفحة 4.
xpsOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<int32_t>({0, 1, 3})));

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

## انظر أيضًا

* Class [PageSet](../../pageset/)
* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
