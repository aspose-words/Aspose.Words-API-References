---
title: "Aspose::Words::Rendering::ThumbnailGeneratingOptions class"
linktitle: "ThumbnailGeneratingOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Rendering::ThumbnailGeneratingOptions class. C++'de bir belge için küçük resim oluştururken ek seçenekleri belirtmek için kullanılabilir."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class


Bir belge için küçük resim oluştururken ek seçenekleri belirtmek için kullanılabilir.

```cpp
class ThumbnailGeneratingOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_GenerateFromFirstPage](./get_generatefromfirstpage/)() const | Belgenin ilk sayfasından mı yoksa ilk görüntüsünden mi küçük resim oluşturulacağını belirtir. |
| [get_ThumbnailSize](./get_thumbnailsize/)() const | Oluşturulan küçük resmin piksel cinsinden boyutu. Varsayılan değer 600x900'dır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_GenerateFromFirstPage](./set_generatefromfirstpage/)(bool) | Ayarlayıcı for [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage](./get_generatefromfirstpage/). |
| [set_ThumbnailSize](./set_thumbnailsize/)(System::Drawing::Size) | Ayarlayıcı for [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize](./get_thumbnailsize/). |
| [ThumbnailGeneratingOptions](./thumbnailgeneratingoptions/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
