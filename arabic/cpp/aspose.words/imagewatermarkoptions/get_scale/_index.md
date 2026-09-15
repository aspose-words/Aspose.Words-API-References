---
title: "Aspose::Words::ImageWatermarkOptions::get_Scale طريقة"
linktitle: "get_Scale"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ImageWatermarkOptions::get_Scale طريقة. يحصل على أو يضبط عامل المقياس المعبر عنه ككسر من الصورة. القيمة الافتراضية هي 0 - تلقائي في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/imagewatermarkoptions/get_scale/
---
## ImageWatermarkOptions::get_Scale method


يحصل أو يضبط معامل المقياس معبرًا ككسر من الصورة. القيمة الافتراضية هي 0 - تلقائي.

```cpp
double Aspose::Words::ImageWatermarkOptions::get_Scale() const
```

## ملاحظات


القيم الصالحة تتراوح من 0 إلى 65.5 شاملًا.

التحجيم التلقائي يعني أن العلامة المائية سيتم تحجيمها إلى أقصى عرض وأقصى ارتفاع بالنسبة إلى هوامش الصفحة.

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
