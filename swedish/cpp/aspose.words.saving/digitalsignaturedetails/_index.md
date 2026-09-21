---
title: "Aspose::Words::Saving::DigitalSignatureDetails-klass"
linktitle: "DigitalSignatureDetails"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::DigitalSignatureDetails-klass. Innehåller detaljer för att signera ett dokument med en digital signatur i C++."
type: docs
weight: 2500
url: /sv/cpp/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class


Innehåller detaljer för att signera ett dokument med en digital signatur.

```cpp
class DigitalSignatureDetails : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [DigitalSignatureDetails](./digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Initierar en ny instans av klassen [DigitalSignatureDetails](./). |
| [get_CertificateHolder](./get_certificateholder/)() const | Hämtar eller anger ett [CertificateHolder](./get_certificateholder/)‑objekt som innehåller certifikatet som används för att signera ett dokument. |
| [get_SignOptions](./get_signoptions/)() const | Hämtar eller anger ett [SignOptions](./get_signoptions/)‑objekt som används för att signera ett dokument. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Sättare för [Aspose::Words::Saving::DigitalSignatureDetails::get_CertificateHolder](./get_certificateholder/). |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Sättare för [Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions](./get_signoptions/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man signerar ett OOXML-dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Some comments");
signOptions->set_SignTime(System::DateTime::get_Now());
auto digitalSignatureDetails = System::MakeObject<Aspose::Words::Saving::DigitalSignatureDetails>(certificateHolder, signOptions);

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_DigitalSignatureDetails(digitalSignatureDetails);

ASPOSE_ASSERT_EQ(certificateHolder, digitalSignatureDetails->get_CertificateHolder());
ASSERT_EQ(u"Some comments", digitalSignatureDetails->get_SignOptions()->get_Comments());

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.DigitalSignature.docx", saveOptions);
```

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
