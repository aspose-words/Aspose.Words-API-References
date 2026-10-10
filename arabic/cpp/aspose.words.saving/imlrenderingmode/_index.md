---
title: "Aspose::Words::Saving::ImlRenderingMode enum"
linktitle: "ImlRenderingMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::ImlRenderingMode enum. يحدد كيفية تحويل كائنات الحبر (InkML) إلى تنسيقات صفحات ثابتة في C++."
type: docs
weight: 66000
url: /ar/cpp/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enum


يحدد كيفية عرض كائنات الحبر (InkML) إلى صيغ الصفحات الثابتة.

```cpp
enum class ImlRenderingMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| بديل | 0 | إذا كان الشكل البديل متاحًا لكائن الحبر (InkML)، تقوم Aspose.Words برسم الشكل البديل بدلاً من InkML. |
| InkML | 1 | Aspose.Words يتجاهل الشكل الاحتياطي لكائن الحبر (InkML) ويعرض InkML نفسه. هذا هو الوضع الافتراضي. |


## أمثلة



يعرض كيفية عرض كائن الحبر.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Ink object.docx");

// Set 'ImlRenderingMode.InkML' يتجاهل الشكل الاحتياطي لكائن الحبر (InkML) ويعرض InkML نفسه.
// إذا كانت نتيجة العرض غير مرضية،
// يرجى استخدام 'ImlRenderingMode.Fallback' للحصول على نتيجة مشابهة للإصدارات السابقة.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
saveOptions->set_ImlRenderingMode(Aspose::Words::Saving::ImlRenderingMode::InkML);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
