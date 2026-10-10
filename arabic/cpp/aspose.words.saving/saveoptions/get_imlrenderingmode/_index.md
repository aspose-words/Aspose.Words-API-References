---
title: "Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode method"
linktitle: "get_ImlRenderingMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode method. يحصل على أو يضبط قيمة تحدد كيفية عرض كائنات الحبر (InkML) في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.saving/saveoptions/get_imlrenderingmode/
---
## SaveOptions::get_ImlRenderingMode method


يحصل أو يعيّن قيمة تحدد كيفية عرض كائنات الحبر (InkML).

```cpp
Aspose::Words::Saving::ImlRenderingMode Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode() const
```

## ملاحظات


القيمة الافتراضية هي [InkML](../../imlrenderingmode/).

يتم استخدام هذه الخاصية عندما يتم تصدير المستند إلى تنسيقات صفحات ثابتة.

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

* Enum [ImlRenderingMode](../../imlrenderingmode/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
