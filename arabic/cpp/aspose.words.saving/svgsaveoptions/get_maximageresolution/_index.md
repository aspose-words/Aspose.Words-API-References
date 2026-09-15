---
title: "Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution طريقة"
linktitle: "get_MaxImageResolution"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution طريقة. يحصل على أو يحدد قيمة بوحدة بكسل لكل بوصة تحدد حد دقة الصور النقطية المصدرة. القيمة الافتراضية هي صفر في C++."
type: docs
weight: 4500
url: /ar/cpp/aspose.words.saving/svgsaveoptions/get_maximageresolution/
---
## SvgSaveOptions::get_MaxImageResolution method


يحصل أو يعيّن قيمة بوحدة بكسل لكل بوصة تحدد حد دقة الصور النقطية المصدرة. القيمة الافتراضية هي صفر.

```cpp
int32_t Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution() const
```

## ملاحظات


إذا كانت قيمة هذه الخاصية غير صفرية، فإنها تحد من دقة الصور النقطية المصدرة. أي أن الصور ذات الدقة العالية يتم تقليل عينتها إلى الحد المحدد، بينما تُصدَّر الصور ذات الدقة المنخفضة كما هي.

إذا كانت قيمة هذه الخاصية صفرًا، يتم تصدير جميع الصور النقطية دون إعادة أخذ عينات.

## أمثلة



يوضح كيفية تعيين حد لدقة الصورة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## انظر أيضًا

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
