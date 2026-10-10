---
title: "Aspose::Words::Saving::SaveOutputParameters::get_ContentType yöntemi"
linktitle: "get_ContentType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SaveOutputParameters::get_ContentType yöntemi. C++'ta kaydedilen belgenin türünü belirten Content-Type dizesini (Internet Media Type) döndürür."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.saving/saveoutputparameters/get_contenttype/
---
## SaveOutputParameters::get_ContentType method


Kaydedilen belgenin türünü tanımlayan Content-Type dizesini (Internet Media Type) döndürür.

```cpp
System::String Aspose::Words::Saving::SaveOutputParameters::get_ContentType() const
```


## Örnekler



Bir belgenin kaydetme işleminin çıktı parametrelerine nasıl erişileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Bir belgeyi kaydettikten sonra, yeni oluşturulan çıktı belgesinin Internet Media Type (MIME türü) değerine erişebiliriz.
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.doc");

ASSERT_EQ(u"application/msword", parameters->get_ContentType());

// Bu özellik, kaydetme biçimine bağlı olarak değişir.
parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.pdf");

ASSERT_EQ(u"application/pdf", parameters->get_ContentType());
```

## Ayrıca Bakınız

* Class [SaveOutputParameters](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
