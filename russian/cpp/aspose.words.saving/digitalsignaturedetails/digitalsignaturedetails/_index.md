---
title: "Aspose::Words::Saving::DigitalSignatureDetails::DigitalSignatureDetails конструктор"
linktitle: "DigitalSignatureDetails"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::DigitalSignatureDetails::DigitalSignatureDetails конструктор. Инициализирует новый экземпляр класса DigitalSignatureDetails в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.saving/digitalsignaturedetails/digitalsignaturedetails/
---
## DigitalSignatureDetails::DigitalSignatureDetails constructor


Инициализирует новый экземпляр класса [DigitalSignatureDetails](../).

```cpp
Aspose::Words::Saving::DigitalSignatureDetails::DigitalSignatureDetails(const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certificateHolder, const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> &signOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| certificateHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | Объект, содержащий сам сертификат. |
| signOptions | const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\& | Параметры подписи, используемые для подписи документа. |

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

* Class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* Class [SignOptions](../../../aspose.words.digitalsignatures/signoptions/)
* Class [DigitalSignatureDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
