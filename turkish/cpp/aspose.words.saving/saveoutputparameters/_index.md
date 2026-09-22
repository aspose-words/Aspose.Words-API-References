---
title: "Aspose::Words::Saving::SaveOutputParameters class"
linktitle: "SaveOutputParameters"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SaveOutputParameters class. Bu nesne, bir belge kaydedildikten sonra çağırıcıya döndürülür ve kaydetme işlemi sırasında oluşturulan veya hesaplanan ek bilgileri içerir. Çağırıcı bu nesneyi kullanabilir veya yok sayabilir. Daha fazla bilgi edinmek için C++'taki belge makalesini ziyaret edin."
type: docs
weight: 30000
url: /tr/cpp/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class


Bu nesne, bir belge kaydedildikten sonra çağırıcıya döndürülür ve kaydetme işlemi sırasında oluşturulan veya hesaplanan ek bilgileri içerir. Çağırıcı bu nesneyi kullanabilir veya yok sayabilir. Daha fazla bilgi için, [Bir Belgeyi Kaydet](https://docs.aspose.com/words/cpp/save-a-document/) dokümantasyon makalesini ziyaret edin.

```cpp
class SaveOutputParameters : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_ContentType](./get_contenttype/)() const | Kaydedilen belgenin türünü tanımlayan Content-Type dizesini (Internet Media Type) döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
