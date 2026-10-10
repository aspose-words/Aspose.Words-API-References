---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureCollection::get_Count yöntemi"
linktitle: "get_Count"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureCollection::get_Count yöntemi. Koleksiyonda bulunan eleman sayısını C++'ta alır."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.digitalsignatures/digitalsignaturecollection/get_count/
---
## DigitalSignatureCollection::get_Count method


Koleksiyonda bulunan eleman sayısını alır.

```cpp
int32_t Aspose::Words::DigitalSignatures::DigitalSignatureCollection::get_Count()
```


## Örnekler



X.509 sertifikalarıyla belgelerin nasıl imzalanacağını gösterir.
```cpp
// Belgenin imzalanmadığını doğrulayın.
ASSERT_FALSE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx")->get_HasDigitalSignature());

// Belgeyi imzalamak için kullanacağımız bir PKCS12 dosyasından CertificateHolder nesnesi oluşturun.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);

// Yerel dosya sistemine imzalı bir belge kopyası kaydetmenin iki yolu vardır:
// 1 - Belgeyi yerel sistem dosya adıyla belirleyin ve imzalı bir kopyayı başka bir dosya adıyla belirtilen konuma kaydedin.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 - Belgeyi bir akıştan alın ve imzalı bir kopyayı başka bir akışa kaydedin.
{
    auto inDoc = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// Lütfen belgenin tüm dijital imzalarının geçerli olduğunu doğrulayın ve ayrıntılarını kontrol edin.
auto signedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.DigitalSignature.docx");
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(1, digitalSignatureCollection->get_Count());
ASSERT_EQ(Aspose::Words::DigitalSignatures::DigitalSignatureType::XmlDsig, digitalSignatureCollection->idx_get(0)->get_SignatureType());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName());
```

## Ayrıca Bakınız

* Class [DigitalSignatureCollection](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
