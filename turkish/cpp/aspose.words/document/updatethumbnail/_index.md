---
title: "Aspose::Words::Document::UpdateThumbnail metodu"
linktitle: "UpdateThumbnail"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::UpdateThumbnail metodu. Belgenin küçük resmini varsayılan seçenekleri kullanarak günceller (C++)."
type: docs
weight: 100000
url: /tr/cpp/aspose.words/document/updatethumbnail/
---
## Document::UpdateThumbnail() method


Belgenin [Thumbnail](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) öğesini varsayılan seçenekleri kullanarak günceller.

```cpp
void Aspose::Words::Document::UpdateThumbnail()
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::UpdateThumbnail(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) method


Belgenin [Thumbnail](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) öğesini belirtilen seçeneklere göre günceller.

```cpp
void Aspose::Words::Document::UpdateThumbnail(const System::SharedPtr<Aspose::Words::Rendering::ThumbnailGeneratingOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| seçenekler | const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\& | Kullanılacak oluşturma seçenekleri. |

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

* Class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
