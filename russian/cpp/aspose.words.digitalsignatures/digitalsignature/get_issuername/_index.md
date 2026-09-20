---
title: "Метод Aspose::Words::DigitalSignatures::DigitalSignature::get_IssuerName"
linktitle: "get_IssuerName"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DigitalSignatures::DigitalSignature::get_IssuerName. Возвращает отличительное имя субъекта сертификата издателя на C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.digitalsignatures/digitalsignature/get_issuername/
---
## DigitalSignature::get_IssuerName method


Возвращает отличительное имя субъекта сертификата издателя.

```cpp
System::String Aspose::Words::DigitalSignatures::DigitalSignature::get_IssuerName()
```


## Примеры



Показывает, как подписывать документы с помощью сертификатов X.509.
```cpp
// Проверьте, что документ не подписан.
ASSERT_FALSE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx")->get_HasDigitalSignature());

// Создайте объект CertificateHolder из файла PKCS12, который мы будем использовать для подписи документа.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);

// Существует два способа сохранить подписанную копию документа в локальную файловую систему:
// 1 — Укажите документ по имени локального файла системы и сохраните подписанную копию в месте, указанном другим именем файла.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 — Возьмите документ из потока и сохраните подписанную копию в другой поток.
{
    auto inDoc = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// Пожалуйста, проверьте, что все цифровые подписи документа действительны, и проверьте их детали.
auto signedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.DigitalSignature.docx");
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(1, digitalSignatureCollection->get_Count());
ASSERT_EQ(Aspose::Words::DigitalSignatures::DigitalSignatureType::XmlDsig, digitalSignatureCollection->idx_get(0)->get_SignatureType());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName());
```

## См. также

* Class [DigitalSignature](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
