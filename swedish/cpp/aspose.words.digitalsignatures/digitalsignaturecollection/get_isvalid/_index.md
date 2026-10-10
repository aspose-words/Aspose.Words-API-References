---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureCollection::get_IsValid metod"
linktitle: "get_IsValid"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureCollection::get_IsValid metod. Returnerar true om alla digitala signaturer i denna samling är giltiga och dokumentet inte har manipulerats. Returnerar också true om det inte finns några digitala signaturer. Returnerar false om minst en digital signatur är ogiltig i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.digitalsignatures/digitalsignaturecollection/get_isvalid/
---
## DigitalSignatureCollection::get_IsValid method


Returnerar **true** om alla digitala signaturer i den här samlingen är giltiga och dokumentet inte har manipulerats. Returnerar också **true** om det inte finns några digitala signaturer. Returnerar **false** om minst en digital signatur är ogiltig.

```cpp
bool Aspose::Words::DigitalSignatures::DigitalSignatureCollection::get_IsValid()
```


## Exempel



Visar hur man signerar dokument med X.509‑certifikat.
```cpp
// Verifiera att ett dokument inte är signerat.
ASSERT_FALSE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx")->get_HasDigitalSignature());

// Skapa ett CertificateHolder‑objekt från en PKCS12‑fil, som vi kommer att använda för att signera dokumentet.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);

// Det finns två sätt att spara en signerad kopia av ett dokument till det lokala filsystemet:
// 1 - Ange ett dokument med ett lokalt filnamn och spara en signerad kopia på en plats som specificeras av ett annat filnamn.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 - Hämta ett dokument från en ström och spara en signerad kopia till en annan ström.
{
    auto inDoc = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// Verifiera att alla dokumentets digitala signaturer är giltiga och kontrollera deras detaljer.
auto signedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.DigitalSignature.docx");
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(1, digitalSignatureCollection->get_Count());
ASSERT_EQ(Aspose::Words::DigitalSignatures::DigitalSignatureType::XmlDsig, digitalSignatureCollection->idx_get(0)->get_SignatureType());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName());
```

## Se även

* Class [DigitalSignatureCollection](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
