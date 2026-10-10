---
title: "Aspose::Words::Saving::ImageSaveOptions::get_ImageSize yöntemi"
linktitle: "get_ImageSize"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ImageSaveOptions::get_ImageSize yöntemi. C++'ta oluşturulan bir görüntünün piksel cinsinden boyutunu alır veya ayarlar."
type: docs
weight: 7500
url: /tr/cpp/aspose.words.saving/imagesaveoptions/get_imagesize/
---
## ImageSaveOptions::get_ImageSize method


Oluşturulan bir görüntünün boyutunu piksel cinsinden alır veya ayarlar.

```cpp
System::Drawing::Size Aspose::Words::Saving::ImageSaveOptions::get_ImageSize() const
```

## Açıklamalar


Bu özellik yalnızca raster görüntü formatlarına kaydedilirken etkili olur.

Varsayılan değer (0 x 0)'dır, bu da oluşturulan görüntünün boyutunun nokta cinsinden görüntü boyutuna, belirtilen çözünürlüğe ve ölçeğe göre hesaplanacağı anlamına gelir.

## Örnekler



Bir belgenin her sayfasını ayrı bir TIFF görüntüsüne nasıl render edeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Belgenin "Save" yöntemine geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// Bu yöntemin belgeyi bir görüntüye render etme şeklini değiştirmek için
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);

for (int32_t i = 0; i < doc->get_PageCount(); i++)
{
    // İlk sayfanın numarasını belirten "PageSet" özelliğini şu sayıdan ayarlayın
    // belirtilen sayfadan belgeyi oluşturmaya başlayın.
    options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(i));
    // Sayfayı 2325x5325 piksel ve 600 dpi olarak dışa aktar.
    options->set_Resolution(600.0f);
    options->set_ImageSize(System::Drawing::Size(2325, 5325));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```

## Ayrıca Bakınız

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
