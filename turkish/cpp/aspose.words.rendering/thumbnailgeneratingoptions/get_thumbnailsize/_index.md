---
title: "Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize metodu"
linktitle: "get_ThumbnailSize"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize metodu. Oluşturulan küçük resmin piksel cinsinden boyutu. Varsayılan değer C++'da 600x900'dır."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.rendering/thumbnailgeneratingoptions/get_thumbnailsize/
---
## ThumbnailGeneratingOptions::get_ThumbnailSize method


Oluşturulan küçük resmin piksel cinsinden boyutu. Varsayılan değer 600x900'dır.

```cpp
System::Drawing::Size Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize() const
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
