---
title: "Clase Aspose::Words::Saving::DigitalSignatureDetails"
linktitle: "DigitalSignatureDetails"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Saving::DigitalSignatureDetails. Contiene detalles para firmar un documento con una firma digital en C++."
type: docs
weight: 2500
url: /es/cpp/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class


Contiene detalles para firmar un documento con una firma digital.

```cpp
class DigitalSignatureDetails : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [DigitalSignatureDetails](./digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Inicializa una nueva instancia de la clase [DigitalSignatureDetails](./). |
| [get_CertificateHolder](./get_certificateholder/)() const | Obtiene o establece un objeto [CertificateHolder](./get_certificateholder/) que contiene el certificado usado para firmar un documento. |
| [get_SignOptions](./get_signoptions/)() const | Obtiene o establece un objeto [SignOptions](./get_signoptions/) usado para firmar un documento. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Método setter para [Aspose::Words::Saving::DigitalSignatureDetails::get_CertificateHolder](./get_certificateholder/). |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Método setter para [Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions](./get_signoptions/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo firmar un documento OOXML.
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

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
