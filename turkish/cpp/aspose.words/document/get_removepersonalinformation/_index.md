---
title: "Aspose::Words::Document::get_RemovePersonalInformation yöntemi"
linktitle: "get_RemovePersonalInformation"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_RemovePersonalInformation yöntemi. Microsoft Word'ün belgeyi C++'ta kaydederken yorumlardan, revizyonlardan ve belge özelliklerinden tüm kullanıcı bilgilerini kaldıracağını belirten bir bayrağı alır veya ayarlar."
type: docs
weight: 45000
url: /tr/cpp/aspose.words/document/get_removepersonalinformation/
---
## Document::get_RemovePersonalInformation method


Microsoft Word'ün belgeyi kaydederken yorumlardan, revizyonlardan ve belge özelliklerinden tüm kullanıcı bilgilerini kaldıracağını gösteren bayrağı alır veya ayarlar.

```cpp
bool Aspose::Words::Document::get_RemovePersonalInformation()
```


## Örnekler



Manuel kaydetme sırasında kişisel bilgilerin kaldırılmasını nasıl etkinleştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Kişisel bilgiler içeren bazı içerikler ekleyin.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
doc->get_BuiltInDocumentProperties()->set_Company(u"Placeholder Inc.");

doc->StartTrackRevisions(doc->get_BuiltInDocumentProperties()->get_Author(), System::DateTime::get_Now());
builder->Write(u"Hello world!");
doc->StopTrackRevisions();

// Bu bayrak, Dosya -> Seçenekler -> Güven Merkezi -> Güven Merkezi Ayarları... -> eşdeğerdir.
// Gizlilik Seçenekleri -> Microsoft Word'de "Kaydetme sırasında dosya özelliklerinden kişisel bilgileri kaldır".
doc->set_RemovePersonalInformation(saveWithoutPersonalInfo);

// Bu seçenek, Aspose.Words kullanılarak yapılan bir kaydetme işlemi sırasında etkili olmayacaktır.
// Kişisel veriler, Microsoft Word kullanarak belgeyi manuel olarak kaydettiğimizde bayrak ayarlı olduğunda belgelerimizden kaldırılacaktır.
doc->Save(get_ArtifactsDir() + u"Document.RemovePersonalInformation.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.RemovePersonalInformation.docx");

ASPOSE_ASSERT_EQ(saveWithoutPersonalInfo, doc->get_RemovePersonalInformation());
ASSERT_EQ(u"John Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Placeholder Inc.", doc->get_BuiltInDocumentProperties()->get_Company());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
