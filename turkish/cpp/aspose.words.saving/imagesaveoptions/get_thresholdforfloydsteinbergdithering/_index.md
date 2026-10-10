---
title: "Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering method"
linktitle: "get_ThresholdForFloydSteinbergDithering"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering yöntemi. Floyd‑Steinberg yönteminde ikilileştirme hatasının değerini belirleyen eşiği alır veya ayarlar. C++'da ImageBinarizationMethod FloydSteinbergDithering olduğunda."
type: docs
weight: 15000
url: /tr/cpp/aspose.words.saving/imagesaveoptions/get_thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions::get_ThresholdForFloydSteinbergDithering method


Floyd-Station yönteminde ikilileştirme hatasının değerini belirleyen eşiği alır veya ayarlar. [ImageBinarizationMethod](../../imagebinarizationmethod/) [FloydSteinbergDithering](../../imagebinarizationmethod/) olduğunda.

```cpp
uint8_t Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering() const
```

## Açıklamalar


Varsayılan değer 128'dir.

## Örnekler



Floyd-Steinberg yöntemini kullanarak bir TIFF görüntüsü oluştururken TIFF ikiliye dönüştürme hata eşiğini nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Belgeyi TIFF olarak kaydettiğimizde, bir SaveOptions nesnesi geçirebiliriz
// Aspose.Words'ün bu görüntüyü oluştururken uygulayacağı titremeyi ayarlamak için.
// "ThresholdForFloydSteinbergDithering" özelliğinin varsayılan değeri 128'dir.
// Daha yüksek değerler genellikle daha karanlık görüntüler üretir.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
options->set_TiffCompression(Aspose::Words::Saving::TiffCompression::Ccitt3);
options->set_TiffBinarizationMethod(Aspose::Words::Saving::ImageBinarizationMethod::FloydSteinbergDithering);
options->set_ThresholdForFloydSteinbergDithering(240);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

## Ayrıca Bakınız

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
