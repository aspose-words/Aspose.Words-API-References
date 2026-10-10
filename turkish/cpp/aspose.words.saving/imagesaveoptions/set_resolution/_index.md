---
title: "Aspose::Words::Saving::ImageSaveOptions::set_Resolution yöntemi"
linktitle: "set_Resolution"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ImageSaveOptions::set_Resolution yöntemi. C++'ta üretilen görüntüler için hem yatay hem de dikey çözünürlüğü inç başına nokta (dpi) cinsinden ayarlar."
type: docs
weight: 30000
url: /tr/cpp/aspose.words.saving/imagesaveoptions/set_resolution/
---
## ImageSaveOptions::set_Resolution method


Oluşturulan görüntüler için hem yatay hem de dikey çözünürlüğü, inç başına nokta (dpi) cinsinden ayarlar.

```cpp
void Aspose::Words::Saving::ImageSaveOptions::set_Resolution(float value)
```

## Açıklamalar


Bu özellik yalnızca raster görüntü formatlarına kaydedilirken etkili olur.

## Örnekler



Bir belgeyi PNG'ye render ederken çözünürlüğü nasıl belirteceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Belgenin "Save" yöntemine geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// Bu yöntemin belgeyi bir görüntüye render etme şeklini değiştirmek için
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// \"Resolution\" özelliğini \"72\" olarak ayarlayarak belgeyi 72dpi'de render edin.
options->set_Resolution(72.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.72dpi.png", options);

// \"Resolution\" özelliğini \"300\" olarak ayarlayarak belgeyi 300dpi'de render edin.
options->set_Resolution(300.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.300dpi.png", options);
```

## Ayrıca Bakınız

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
