---
title: "Aspose::Words::Saving::DigitalSignatureDetails classe"
linktitle: "DigitalSignatureDetails"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Saving::DigitalSignatureDetails. Contiene i dettagli per firmare un documento con una firma digitale in C++."
type: docs
weight: 2500
url: /it/cpp/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class


Contiene i dettagli per firmare un documento con una firma digitale.

```cpp
class DigitalSignatureDetails : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [DigitalSignatureDetails](./digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Inizializza una nuova istanza della classe [DigitalSignatureDetails](./). |
| [get_CertificateHolder](./get_certificateholder/)() const | Ottiene o imposta un oggetto [CertificateHolder](./get_certificateholder/) che contiene il certificato utilizzato per firmare un documento. |
| [get_SignOptions](./get_signoptions/)() const | Ottiene o imposta un oggetto [SignOptions](./get_signoptions/) utilizzato per firmare un documento. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Metodo set per [Aspose::Words::Saving::DigitalSignatureDetails::get_CertificateHolder](./get_certificateholder/). |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Metodo set per [Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions](./get_signoptions/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come firmare un documento OOXML.
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

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
