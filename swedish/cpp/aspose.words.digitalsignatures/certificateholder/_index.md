---
title: "Aspose::Words::DigitalSignatures::CertificateHolder‑klass"
linktitle: "CertificateHolder"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DigitalSignatures::CertificateHolder-klass. Representerar en hållare av X509Certificate2-instans. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class


Representerar en behållare för en **X509Certificate2**‑instans. För att lära dig mer, besök dokumentationsartikeln [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class CertificateHolder : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) | Skapar [CertificateHolder](./)-objekt med bytearray från PKCS12-lagring och dess lösenord. |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) | Skapar [CertificateHolder](./)-objekt med bytearray från PKCS12-lagring och dess lösenord. |
| static [Create](./create/)(const System::String\&, const System::String\&) | Skapar [CertificateHolder](./)-objekt med sökväg till PKCS12-lagring och dess lösenord. |
| static [Create](./create/)(const System::String\&, const System::String\&, const System::String\&) | Skapar [CertificateHolder](./)-objekt med sökväg till PKCS12-lagring, dess lösenord och aliaset som används för att hitta privat nyckel och certifikat. |
| [get_Certificate](./get_certificate/)() | Returnerar instansen av **X509Certificate2** som innehåller privata och offentliga nycklar samt certifikatkedja. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Anmärkningar


[CertificateHolder](./) can be created by static factory methods only. It contains an instance of **X509Certificate2** which is used to introduce private, public keys and certificate chains into the system. This class is applied in [DigitalSignatureUtil](../digitalsignatureutil/) and [PdfDigitalSignatureDetails](../../aspose.words.saving/pdfdigitalsignaturedetails/) instead of obsolete methods with **X509Certificate2** as parameters.

## Exempel



Visar hur man digitalt signerar dokument.
```cpp
// Skapa ett X.509‑certifikat från en PKCS#12‑butik, som bör innehålla en privat nyckel.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Skapa en kommentar och ett datum som kommer att tillämpas med vår nya digitala signatur.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Hämta ett osignerat dokument från det lokala filsystemet via en filström,
// sedan skapa en signerad kopia av den bestämd av filnamnet på utdatafilströmmen.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```


Visar hur man signerar en krypterad dokumentfil.
```cpp
// Skapa ett X.509‑certifikat från en PKCS#12‑butik, som bör innehålla en privat nyckel.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Skapa en kommentar, datum och dekrypteringslösenord som kommer att tillämpas med vår nya digitala signatur.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

// Ange ett lokalt systemfilnamn för det osignerade inmatningsdokumentet och ett utdatafilnamn för dess nya digitalt signerade kopia.
System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.DecryptionPassword.docx";

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## Se även

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
