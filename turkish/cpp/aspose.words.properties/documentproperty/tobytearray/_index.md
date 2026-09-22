---
title: "Aspose::Words::Properties::DocumentProperty::ToByteArray yöntemi"
linktitle: "ToByteArray"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::DocumentProperty::ToByteArray yöntemi. Özellik değerini C++'ta bayt dizisi olarak döndürür."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty::ToByteArray method


Özellik değerini bayt dizisi olarak döndürür.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::DocumentProperty::ToByteArray()
```

## Açıklamalar


Özellik tipi [ByteArray](../../propertytype/) değilse bir istisna fırlatır.

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

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
