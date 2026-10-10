---
title: "Aspose::Words::Saving::DigitalSignatureDetails class"
linktitle: "DigitalSignatureDetails"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::DigitalSignatureDetails sınıfı. C++'ta bir belgeyi dijital imza ile imzalamak için ayrıntıları içerir."
type: docs
weight: 2500
url: /tr/cpp/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class


Bir belgeyi dijital imza ile imzalamak için ayrıntıları içerir.

```cpp
class DigitalSignatureDetails : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [DigitalSignatureDetails](./digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Yeni bir [DigitalSignatureDetails](./) sınıfı örneği başlatır. |
| [get_CertificateHolder](./get_certificateholder/)() const | [CertificateHolder](./get_certificateholder/) nesnesini alır veya ayarlar; bu nesne belgeyi imzalamak için kullanılan sertifikayı içerir. |
| [get_SignOptions](./get_signoptions/)() const | Belgeyi imzalamak için kullanılan bir [SignOptions](./get_signoptions/) nesnesini alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | [Aspose::Words::Saving::DigitalSignatureDetails::get_CertificateHolder](./get_certificateholder/) için ayarlayıcı. |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | [Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions](./get_signoptions/) için ayarlayıcı. |
| static [Type](./type/)() |  |

## Örnekler



OOXML belgesinin nasıl imzalanacağını gösterir.
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

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
