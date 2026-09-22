---
title: "Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod yöntemi"
linktitle: "get_TiffBinarizationMethod"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod yöntemi. C++'ta SaveFormat Tiff ve TiffCompression Ccitt3 veya Ccitt4 olduğunda görüntüleri 1 bpp formatına dönüştürürken kullanılan yöntemi alır veya ayarlar."
type: docs
weight: 16000
url: /tr/cpp/aspose.words.saving/imagesaveoptions/get_tiffbinarizationmethod/
---
## ImageSaveOptions::get_TiffBinarizationMethod method


[SaveFormat](../get_saveformat/) [Tiff](../../../aspose.words/saveformat/) olduğunda ve [TiffCompression](../get_tiffcompression/) [Ccitt3](../../tiffcompression/) veya [Ccitt4](../../tiffcompression/) eşit olduğunda görüntüleri 1 bpp formatına dönüştürürken kullanılan yöntemi alır veya ayarlar.

```cpp
Aspose::Words::Saving::ImageBinarizationMethod Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod() const
```

## Açıklamalar


Varsayılan değer [Threshold](../../imagebinarizationmethod/) dir.

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

* Enum [ImageBinarizationMethod](../../imagebinarizationmethod/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
