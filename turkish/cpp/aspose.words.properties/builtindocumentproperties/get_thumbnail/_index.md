---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail method"
linktitle: "get_Thumbnail"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail yöntemi. C++'ta belgenin küçük resmini alır veya ayarlar."
type: docs
weight: 28000
url: /tr/cpp/aspose.words.properties/builtindocumentproperties/get_thumbnail/
---
## BuiltInDocumentProperties::get_Thumbnail method


Belgenin küçük resmini alır veya ayarlar.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail()
```

## Açıklamalar


Şimdilik bu özellik yalnızca bir belge ePub formatına dışa aktarılırken kullanılır, diğer belge formatlarından okunmaz ve onlara yazılmaz.

İsteğe bağlı herhangi bir formatta görüntü bu özelliğe ayarlanabilir, ancak format dışa aktarım sırasında kontrol edilir.

Yalnızca gif, jpeg ve png görüntüleri ePub yayıncılığı için kullanılabilir.

## Örnekler



Bir belgeye, Epub olarak kaydettiğimizde nasıl bir küçük resim ekleyeceğimizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Eğer eklediğimiz görüntü verisini içeren "Thumbnail" özelliğine sahip bir belgeyi Epub olarak kaydedersek,
// belgeyi açan bir okuyucu, ilk sayfadan önce görüntüyü gösterebilir.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

System::ArrayPtr<uint8_t> thumbnailBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");
properties->set_Thumbnail(thumbnailBytes);

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.epub");

// Bir belgenin küçük resim görüntüsünü çıkarabilir ve yerel dosya sistemine kaydedebiliriz.
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> thumbnail = doc->get_BuiltInDocumentProperties()->idx_get(u"Thumbnail");
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.gif", thumbnail->ToByteArray());
```

## Ayrıca Bakınız

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
