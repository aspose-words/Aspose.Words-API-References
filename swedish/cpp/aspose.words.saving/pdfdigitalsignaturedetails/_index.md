---
title: "Aspose::Words::Saving::PdfDigitalSignatureDetails class"
linktitle: "PdfDigitalSignatureDetails"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PdfDigitalSignatureDetails class. Innehåller detaljer för signering av ett PDF-dokument med en digital signatur i C++."
type: docs
weight: 22000
url: /sv/cpp/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class


Innehåller detaljer för att signera ett PDF-dokument med en digital signatur.

```cpp
class PdfDigitalSignatureDetails : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | Returnerar certifikathållarobjektet som innehåller certifikatet som användes för att signera dokumentet. |
| [get_HashAlgorithm](./get_hashalgorithm/)() const | Hämtar hash-algoritmen. |
| [get_Location](./get_location/)() const | Hämtar signeringsplatsen. |
| [get_Reason](./get_reason/)() const | Hämtar anledningen till signeringen. |
| [get_SignatureDate](./get_signaturedate/)() const | Hämtar eller anger datumet för signeringen. |
| [get_TimestampSettings](./get_timestampsettings/)() const | Hämtar eller anger inställningarna för digital signatur tidsstämpel. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)() | Initierar en instans av denna klass. |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::String\&, const System::String\&, System::DateTime) | Initierar en instans av denna klass. |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Returnerar certifikathållarobjektet som innehåller certifikatet som användes för att signera dokumentet. |
| [set_HashAlgorithm](./set_hashalgorithm/)(Aspose::Words::Saving::PdfDigitalSignatureHashAlgorithm) | Anger hash-algoritmen. |
| [set_Location](./set_location/)(const System::String\&) | Anger signeringsplatsen. |
| [set_Reason](./set_reason/)(const System::String\&) | Anger anledningen till signeringen. |
| [set_SignatureDate](./set_signaturedate/)(System::DateTime) | Sättare för [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_SignatureDate](./get_signaturedate/). |
| [set_TimestampSettings](./set_timestampsettings/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureTimestampSettings\>\&) | Sättare för [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_TimestampSettings](./get_timestampsettings/). |
| static [Type](./type/)() |  |
## Anmärkningar


För närvarande är digital signering av PDF-dokument endast tillgänglig på .NET 3.5 eller högre.

För att digitalt signera ett PDF-dokument när det skapas av Aspose.Words, sätt egenskapen [DigitalSignatureDetails](../pdfsaveoptions/get_digitalsignaturedetails/) till ett giltigt [PdfDigitalSignatureDetails](./)-objekt och spara sedan dokumentet i PDF-format genom att skicka [PdfSaveOptions](../pdfsaveoptions/) som en parameter till [Save()](../)-metoden.

Aspose.Words skapar en PKCS#7-signatur över hela PDF-dokumentet och använder filtret \"Adobe.PPKMS\" och subfiltret \"adbe.pkcs7.sha1\" när en digital signatur skapas.

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
