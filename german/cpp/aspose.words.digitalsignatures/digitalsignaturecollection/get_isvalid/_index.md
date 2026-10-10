---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureCollection::get_IsValid Methode"
linktitle: "get_IsValid"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureCollection::get_IsValid Methode. Gibt true zurück, wenn alle digitalen Signaturen in dieser Sammlung gültig sind und das Dokument nicht manipuliert wurde. Gibt ebenfalls true zurück, wenn keine digitalen Signaturen vorhanden sind. Gibt false zurück, wenn mindestens eine digitale Signatur in C++ ungültig ist."
type: docs
weight: 8000
url: /de/cpp/aspose.words.digitalsignatures/digitalsignaturecollection/get_isvalid/
---
## DigitalSignatureCollection::get_IsValid method


Gibt **true** zurück, wenn alle digitalen Signaturen in dieser Sammlung gültig sind und das Dokument nicht manipuliert wurde. Gibt außerdem **true** zurück, wenn keine digitalen Signaturen vorhanden sind. Gibt **false** zurück, wenn mindestens eine digitale Signatur ungültig ist.

```cpp
bool Aspose::Words::DigitalSignatures::DigitalSignatureCollection::get_IsValid()
```


## Beispiele



Zeigt, wie man Dokumente mit X.509-Zertifikaten signiert.
```cpp
// Überprüfen Sie, dass ein Dokument nicht signiert ist.
ASSERT_FALSE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx")->get_HasDigitalSignature());

// Erstellen Sie ein CertificateHolder‑Objekt aus einer PKCS12‑Datei, das wir zum Signieren des Dokuments verwenden werden.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);

// Es gibt zwei Möglichkeiten, eine signierte Kopie eines Dokuments im lokalen Dateisystem zu speichern:
// 1 - Bezeichnen Sie ein Dokument anhand eines lokalen Systemdateinamens und speichern Sie eine signierte Kopie an einem Ort, der durch einen anderen Dateinamen angegeben ist.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 - Nehmen Sie ein Dokument aus einem Stream und speichern Sie eine signierte Kopie in einen anderen Stream.
{
    auto inDoc = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// Bitte überprüfen Sie, dass alle digitalen Signaturen des Dokuments gültig sind, und prüfen Sie deren Details.
auto signedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.DigitalSignature.docx");
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(1, digitalSignatureCollection->get_Count());
ASSERT_EQ(Aspose::Words::DigitalSignatures::DigitalSignatureType::XmlDsig, digitalSignatureCollection->idx_get(0)->get_SignatureType());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName());
```

## Siehe auch

* Class [DigitalSignatureCollection](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
