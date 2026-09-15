---
title: "Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod طريقة"
linktitle: "get_TiffBinarizationMethod"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod طريقة. يحصل أو يضبط الطريقة المستخدمة أثناء تحويل الصور إلى تنسيق 1 bpp عندما يكون SaveFormat هو Tiff و TiffCompression يساوي Ccitt3 أو Ccitt4 في C++."
type: docs
weight: 16000
url: /ar/cpp/aspose.words.saving/imagesaveoptions/get_tiffbinarizationmethod/
---
## ImageSaveOptions::get_TiffBinarizationMethod method


يحصل أو يضبط الطريقة المستخدمة أثناء تحويل الصور إلى تنسيق 1 bpp عندما يكون [SaveFormat](../get_saveformat/) هو [Tiff](../../../aspose.words/saveformat/) و [TiffCompression](../get_tiffcompression/) يساوي [Ccitt3](../../tiffcompression/) أو [Ccitt4](../../tiffcompression/).

```cpp
Aspose::Words::Saving::ImageBinarizationMethod Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod() const
```

## ملاحظات


القيمة الافتراضية هي [Threshold](../../imagebinarizationmethod/).

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

* Enum [ImageBinarizationMethod](../../imagebinarizationmethod/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
