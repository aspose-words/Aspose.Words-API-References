---
title: "Aspose::Words::Document::get_DigitalSignatures Methode"
linktitle: "get_DigitalSignatures"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_DigitalSignatures Methode. Gibt die Sammlung digitaler Signaturen für dieses Dokument und deren Validierungsergebnisse in C++ zurück."
type: docs
weight: 21000
url: /de/cpp/aspose.words/document/get_digitalsignatures/
---
## Document::get_DigitalSignatures method


Liest die Sammlung digitaler Signaturen für dieses Dokument und deren Validierungsergebnisse.

```cpp
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> Aspose::Words::Document::get_DigitalSignatures() const
```

## Hinweise


Diese Sammlung enthält digitale Signaturen, die aus dem Originaldokument geladen wurden. Diese digitalen Signaturen werden nicht gespeichert, wenn Sie dieses [Document](../)-Objekt in eine Datei oder einen Stream speichern, da das Speichern oder Konvertieren ein Dokument erzeugt, das vom Original abweicht, und die ursprünglichen digitalen Signaturen dann nicht mehr gültig sind.

Diese Sammlung ist niemals **null**. Wenn das Dokument nicht signiert ist, enthält sie null Elemente.

## Beispiele



Zeigt, wie man jede Signatur in einem Dokument validiert und Informationen darüber anzeigt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Digitally signed.docx");

for (auto&& signature : doc->get_DigitalSignatures())
{
    std::cout << System::String::Format(u"{0} signature: ", (signature->get_IsValid() ? System::String(u"Valid") : System::String(u"Invalid"))) << std::endl;
    std::cout << System::String::Format(u"\tReason:\t{0}", signature->get_Comments()) << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", signature->get_SignatureType()) << std::endl;
    std::cout << System::String::Format(u"\tSign time:\t{0}", signature->get_SignTime()) << std::endl;
    std::cout << System::String::Format(u"\tSubject name:\t{0}", signature->get_CertificateHolder()->get_Certificate()->get_SubjectName()) << std::endl;
    std::cout << System::String::Format(u"\tIssuer name:\t{0}", signature->get_CertificateHolder()->get_Certificate()->get_IssuerName()->get_Name()) << std::endl;
    std::cout << std::endl;
}
```


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

* Class [DigitalSignatureCollection](../../../aspose.words.digitalsignatures/digitalsignaturecollection/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
