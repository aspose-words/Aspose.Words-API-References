---
title: "فئة Aspose::Words::ImageWatermarkOptions"
linktitle: "ImageWatermarkOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::ImageWatermarkOptions. تحتوي على خيارات يمكن تحديدها عند إضافة علامة مائية بصورة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 34000
url: /ar/cpp/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class


يحتوي على خيارات يمكن تحديدها عند إضافة علامة مائية بصورة. لمعرفة المزيد، زر مقالة الوثائق [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/)

```cpp
class ImageWatermarkOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_IsWashout](./get_iswashout/)() const | يحصل أو يضبط قيمة منطقية مسؤولة عن تأثير التلاشي للعلامة المائية. القيمة الافتراضية هي **true**. |
| [get_Scale](./get_scale/)() const | يحصل أو يضبط معامل المقياس معبرًا ككسر من الصورة. القيمة الافتراضية هي 0 - تلقائي. |
| [GetType](./gettype/)() const override |  |
| [ImageWatermarkOptions](./imagewatermarkoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsWashout](./set_iswashout/)(bool) | ضابط لـ [Aspose::Words::ImageWatermarkOptions::get_IsWashout](./get_iswashout/). |
| [set_Scale](./set_scale/)(double) | ضابط لـ [Aspose::Words::ImageWatermarkOptions::get_Scale](./get_scale/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
