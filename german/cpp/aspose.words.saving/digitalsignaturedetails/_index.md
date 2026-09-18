---
title: "Aspose::Words::Saving::DigitalSignatureDetails class"
linktitle: "DigitalSignatureDetails"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::DigitalSignatureDetails Klasse. Enthält Details zum Signieren eines Dokuments mit einer digitalen Signatur in C++."
type: docs
weight: 2500
url: /de/cpp/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class


Enthält Details zum Signieren eines Dokuments mit einer digitalen Signatur.

```cpp
class DigitalSignatureDetails : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [DigitalSignatureDetails](./digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Initialisiert eine neue Instanz der Klasse [DigitalSignatureDetails](./). |
| [get_CertificateHolder](./get_certificateholder/)() const | Liest oder setzt ein [CertificateHolder](./get_certificateholder/) Objekt, das das zum Signieren eines Dokuments verwendete Zertifikat enthält. |
| [get_SignOptions](./get_signoptions/)() const | Liest oder setzt ein [SignOptions](./get_signoptions/) Objekt, das zum Signieren eines Dokuments verwendet wird. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Setter für [Aspose::Words::Saving::DigitalSignatureDetails::get_CertificateHolder](./get_certificateholder/). |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Setter für [Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions](./get_signoptions/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man ein OOXML-Dokument signiert.
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

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
