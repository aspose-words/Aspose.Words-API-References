---
title: "Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage metodu"
linktitle: "get_GenerateFromFirstPage"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage metodu. C++'da belgenin ilk sayfasından veya ilk görüntüsünden küçük resim oluşturulup oluşturulmayacağını belirtir."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.rendering/thumbnailgeneratingoptions/get_generatefromfirstpage/
---
## ThumbnailGeneratingOptions::get_GenerateFromFirstPage method


Belgenin ilk sayfasından mı yoksa ilk görüntüsünden mi küçük resim oluşturulacağını belirtir.

```cpp
bool Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage() const
```


## Örnekler



Bir belgenin küçük resmini nasıl güncelleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// .epub formatında bir belgeyi kaydederken küçük resim ayarlamanın iki yolu vardır.
// 1 -  Belgenin ilk sayfasını kullan:
doc->UpdateThumbnail();
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstPage.epub");

// 2 -  Belgede bulunan ilk görüntüyü kullan:
auto options = System::MakeObject<Aspose::Words::Rendering::ThumbnailGeneratingOptions>();
options->set_ThumbnailSize(System::Drawing::Size(400, 400));
options->set_GenerateFromFirstPage(false);

doc->UpdateThumbnail(options);
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstImage.epub");
```

## Ayrıca Bakınız

* Class [ThumbnailGeneratingOptions](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
