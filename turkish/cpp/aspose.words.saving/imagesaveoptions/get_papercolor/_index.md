---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PaperColor yöntemi"
linktitle: "get_PaperColor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ImageSaveOptions::get_PaperColor yöntemi. Oluşturulan görüntüler için arka plan (kağıt) rengini alır veya ayarlar. Varsayılan değer C++'ta Beyaz'dir."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.saving/imagesaveoptions/get_papercolor/
---
## ImageSaveOptions::get_PaperColor method


Oluşturulan görüntüler için arka plan (kağıt) rengini alır veya ayarlar. Varsayılan değer **White**'dır.

```cpp
System::Drawing::Color Aspose::Words::Saving::ImageSaveOptions::get_PaperColor()
```

## Açıklamalar


Kendi arka plan rengini belirten bir belgenin sayfaları render edildiğinde, belge arka plan rengi bu özellikte belirtilen rengi geçersiz kılar.

## Örnekler



Bir Word belgesinin sayfasını şeffaf veya renkli arka planlı bir görüntüye renderlar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Belgenin "Save" yöntemine geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// Bu yöntemin belgeyi bir görüntüye render etme şeklini değiştirmek için
auto imgOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Şeffaf bir renk uygulamak için \"PaperColor\" özelliğini şeffaf bir renge ayarlayın
// belgeyi bir görüntüye render ederken belgeye arka plan ekleyin.
imgOptions->set_PaperColor(System::Drawing::Color::get_Transparent());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// \"PaperColor\" özelliğini opak bir renge ayarlayarak o rengi uygulayın
// belgeyi bir görüntüye render ederken belgeye arka plan olarak
imgOptions->set_PaperColor(System::Drawing::Color::get_LightCoral());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

## Ayrıca Bakınız

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
