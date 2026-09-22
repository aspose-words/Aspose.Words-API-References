---
title: "Aspose::Words::Saving::ImageBinarizationMethod تعداد"
linktitle: "ImageBinarizationMethod"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::ImageBinarizationMethod تعداد. يحدد الطريقة المستخدمة لتحويل الصورة إلى ثنائية في C++."
type: docs
weight: 63000
url: /ar/cpp/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enum


يحدد الطريقة المستخدمة لتحويل الصورة إلى ثنائية.

```cpp
enum class ImageBinarizationMethod
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| الحد | 0 | يحدد طريقة الحد. |
| FloydSteinbergDithering | 1 | يحدد التدرج باستخدام طريقة انتشار الخطأ Floyd‑Steinberg. |


## أمثلة



يظهر كيفية ضبط حد خطأ تحويل TIFF إلى ثنائي عند استخدام طريقة Floyd‑Steinberg لتصيير صورة TIFF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// عند حفظ المستند كملف TIFF، يمكننا تمرير كائن SaveOptions إلى
// ضبط التدرج الذي سيطبقه Aspose.Words عند تصيير هذه الصورة.
// القيمة الافتراضية للخاصية "ThresholdForFloydSteinbergDithering" هي 128.
// القيم الأعلى تميل إلى إنتاج صور أغمق.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
options->set_TiffCompression(Aspose::Words::Saving::TiffCompression::Ccitt3);
options->set_TiffBinarizationMethod(Aspose::Words::Saving::ImageBinarizationMethod::FloydSteinbergDithering);
options->set_ThresholdForFloydSteinbergDithering(240);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
