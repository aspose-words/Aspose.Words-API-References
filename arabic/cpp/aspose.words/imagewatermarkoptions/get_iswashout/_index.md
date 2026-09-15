---
title: "طريقة get_IsWashout في Aspose::Words::ImageWatermarkOptions"
linktitle: "get_IsWashout"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة get_IsWashout في Aspose::Words::ImageWatermarkOptions. يحصل على أو يعيّن قيمة منطقية مسؤولة عن تأثير التلاشي للعلامة المائية. القيمة الافتراضية هي true في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/imagewatermarkoptions/get_iswashout/
---
## ImageWatermarkOptions::get_IsWashout method


يحصل أو يضبط قيمة منطقية مسؤولة عن تأثير التلاشي للعلامة المائية. القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::ImageWatermarkOptions::get_IsWashout() const
```


## أمثلة



يوضح كيفية إنشاء علامة مائية من صورة في نظام الملفات المحلي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// عدّل مظهر العلامة المائية للصورة باستخدام كائن ImageWatermarkOptions،
// ثم مرره أثناء إنشاء علامة مائية من ملف صورة.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// لدينا خيارات مختلفة لإدراج صورة.
// استخدم إحدى الطرق التالية لإضافة علامة مائية صورة.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## انظر أيضًا

* Class [ImageWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
