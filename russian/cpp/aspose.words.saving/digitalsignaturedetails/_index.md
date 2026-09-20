---
title: "Класс Aspose::Words::Saving::DigitalSignatureDetails"
linktitle: "DigitalSignatureDetails"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Saving::DigitalSignatureDetails. Содержит детали для подписания документа цифровой подписью в C++."
type: docs
weight: 2500
url: /ru/cpp/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class


Содержит сведения о подписании документа цифровой подписью.

```cpp
class DigitalSignatureDetails : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [DigitalSignatureDetails](./digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Инициализирует новый экземпляр класса [DigitalSignatureDetails](./). |
| [get_CertificateHolder](./get_certificateholder/)() const | Получает или задает объект [CertificateHolder](./get_certificateholder/), который содержит сертификат, используемый для подписания документа. |
| [get_SignOptions](./get_signoptions/)() const | Получает или задает объект [SignOptions](./get_signoptions/), используемый для подписания документа. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Сеттер для [Aspose::Words::Saving::DigitalSignatureDetails::get_CertificateHolder](./get_certificateholder/). |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Сеттер для [Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions](./get_signoptions/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как подписать документ OOXML.
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

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
