---
title: "Classe Aspose::Words::Saving::DigitalSignatureDetails"
linktitle: "DigitalSignatureDetails"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Saving::DigitalSignatureDetails. Contient les détails pour signer un document avec une signature numérique en C++."
type: docs
weight: 2500
url: /fr/cpp/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class


Contient les détails pour signer un document avec une signature numérique.

```cpp
class DigitalSignatureDetails : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [DigitalSignatureDetails](./digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Initialise une nouvelle instance de la classe [DigitalSignatureDetails](./). |
| [get_CertificateHolder](./get_certificateholder/)() const | Obtient ou définit un objet [CertificateHolder](./get_certificateholder/) qui contient le certificat utilisé pour signer un document. |
| [get_SignOptions](./get_signoptions/)() const | Obtient ou définit un objet [SignOptions](./get_signoptions/) utilisé pour signer un document. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Définisseur pour [Aspose::Words::Saving::DigitalSignatureDetails::get_CertificateHolder](./get_certificateholder/). |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Définisseur pour [Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions](./get_signoptions/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment signer un document OOXML.
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

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
