---
title: "Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering طريقة"
linktitle: "get_ThresholdForFloydSteinbergDithering"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering طريقة. يحصل على أو يضبط العتبة التي تحدد قيمة خطأ التثنائي في طريقة Floyd‑Steinberg عندما تكون ImageBinarizationMethod هي FloydSteinbergDithering في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.saving/imagesaveoptions/get_thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions::get_ThresholdForFloydSteinbergDithering method


يحصل على أو يضبط العتبة التي تحدد قيمة خطأ التثنائي في طريقة Floyd‑Steinberg عندما تكون [ImageBinarizationMethod](../../imagebinarizationmethod/) هي [FloydSteinbergDithering](../../imagebinarizationmethod/).

```cpp
uint8_t Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering() const
```

## ملاحظات


القيمة الافتراضية هي 128.

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

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
