---
title: "Aspose::Words::DigitalSignatures::CertificateHolder-Klasse"
linktitle: "CertificateHolder"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DigitalSignatures::CertificateHolder-Klasse. Stellt einen Halter einer X509Certificate2-Instanz dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class


Stellt einen Halter einer **X509Certificate2**-Instanz dar. Weitere Informationen finden Sie im [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) Dokumentationsartikel.

```cpp
class CertificateHolder : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) | Erstellt ein [CertificateHolder](./)-Objekt mithilfe des Byte-Arrays des PKCS12-Stores und dessen Passwort. |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) | Erstellt ein [CertificateHolder](./)-Objekt mithilfe des Byte-Arrays des PKCS12-Stores und dessen Passwort. |
| static [Create](./create/)(const System::String\&, const System::String\&) | Erstellt ein [CertificateHolder](./)-Objekt mithilfe des Pfads zum PKCS12-Store und dessen Passwort. |
| static [Create](./create/)(const System::String\&, const System::String\&, const System::String\&) | Erstellt ein [CertificateHolder](./)-Objekt mithilfe des Pfads zum PKCS12-Store, dessen Passwort und dem Alias, über den der private Schlüssel und das Zertifikat gefunden werden. |
| [get_Certificate](./get_certificate/)() | Gibt die Instanz von **X509Certificate2** zurück, die private und öffentliche Schlüssel sowie die Zertifikatskette enthält. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Hinweise


[CertificateHolder](./) can be created by static factory methods only. It contains an instance of **X509Certificate2** which is used to introduce private, public keys and certificate chains into the system. This class is applied in [DigitalSignatureUtil](../digitalsignatureutil/) and [PdfDigitalSignatureDetails](../../aspose.words.saving/pdfdigitalsignaturedetails/) instead of obsolete methods with **X509Certificate2** as parameters.

## Beispiele



Zeigt, wie man Dokumente digital signiert.
```cpp
// Erstellen Sie ein X.509-Zertifikat aus einem PKCS#12-Store, der einen privaten Schlüssel enthalten sollte.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Erstellen Sie einen Kommentar und ein Datum, die mit unserer neuen digitalen Signatur angewendet werden.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Nehmen Sie ein unsigniertes Dokument aus dem lokalen Dateisystem über einen Dateistream,
// und erstellen Sie dann eine signierte Kopie davon, bestimmt durch den Dateinamen des Ausgabedateistreams.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```


Zeigt, wie man eine verschlüsselte Dokumentdatei signiert.
```cpp
// Erstellen Sie ein X.509-Zertifikat aus einem PKCS#12-Store, der einen privaten Schlüssel enthalten sollte.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Erstellt einen Kommentar, ein Datum und ein Entschlüsselungspasswort, die mit unserer neuen digitalen Signatur angewendet werden.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

// Legt einen lokalen Systemdateinamen für das unsignierte Eingabedokument fest und einen Ausgabedateinamen für dessen neu digital signierte Kopie.
System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.DecryptionPassword.docx";

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## Siehe auch

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
