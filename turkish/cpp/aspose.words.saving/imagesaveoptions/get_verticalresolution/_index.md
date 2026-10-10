---
title: "Aspose::Words::Saving::ImageSaveOptions::get_VerticalResolution yöntemi"
linktitle: "get_VerticalResolution"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ImageSaveOptions::get_VerticalResolution yöntemi. C++'de oluşturulan görüntüler için dikey çözünürlüğü nokta başına inç cinsinden alır veya ayarlar."
type: docs
weight: 19000
url: /tr/cpp/aspose.words.saving/imagesaveoptions/get_verticalresolution/
---
## ImageSaveOptions::get_VerticalResolution method


Oluşturulan görüntüler için dikey çözünürlüğü, inç başına nokta (dpi) cinsinden alır veya ayarlar.

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_VerticalResolution() const
```

## Açıklamalar


Bu özellik yalnızca raster görüntü formatlarına kaydedilirken etkili olur ve çıktı boyutunu piksel olarak etkiler.

Varsayılan değer 96'dır.

## Örnekler



Aspose.Words bir belgeyi görüntüye dönüştürürken görüntünün nasıl düzenleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Belgeyi görüntü olarak kaydettiğimizde, bir SaveOptions nesnesi geçirebiliriz
// kaydetme işlemi görüntüyü işlerken resmi düzenleyin.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Bu özellikleri, görüntünün parlaklığını ve kontrastını değiştirmek için ayarlayabiliriz.
// Her ikisi de 0-1 ölçeğinde ve varsayılan olarak 0.5 değerindedir.
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
// Bu özelliklerle yatay ve dikey çözünürlüğü ayarlayabiliriz.
// Bu, görüntünün boyutlarını etkileyecektir.
// Bu özelliklerin varsayılan değeri 96.0'dır, 96dpi çözünürlük için.
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
// Bu özelliği kullanarak görüntüyü ölçeklendirebiliriz. Varsayılan değer 1.0'dır, %100 ölçekleme için.
// Bu özelliği, çözünürlüğü değiştirmekten kaynaklanabilecek görüntü boyutu değişikliklerini ortadan kaldırmak için kullanabiliriz.
options->set_Scale(96.f / 72.f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.EditImage.png", options);
```

## Ayrıca Bakınız

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
