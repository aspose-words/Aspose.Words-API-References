---
title: "Aspose::Words::Saving::XpsSaveOptions::get_DigitalSignatureDetails метод"
linktitle: "get_DigitalSignatureDetails"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::XpsSaveOptions::get_DigitalSignatureDetails метод. Получает или задает объект DigitalSignatureDetails, используемый для подписи документа в C++."
type: docs
weight: 2500
url: /ru/cpp/aspose.words.saving/xpssaveoptions/get_digitalsignaturedetails/
---
## XpsSaveOptions::get_DigitalSignatureDetails method


Получает или задает объект [DigitalSignatureDetails](../../digitalsignaturedetails/) используемый для подписи документа.

```cpp
const System::SharedPtr<Aspose::Words::Saving::DigitalSignatureDetails> & Aspose::Words::Saving::XpsSaveOptions::get_DigitalSignatureDetails() const
```


## Примеры



Показывает, как подписать документ XPS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");
auto options = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
options->set_SignTime(System::DateTime::get_Now());
options->set_Comments(u"Some comments");

auto digitalSignatureDetails = System::MakeObject<Aspose::Words::Saving::DigitalSignatureDetails>(certificateHolder, options);

auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
saveOptions->set_DigitalSignatureDetails(digitalSignatureDetails);

ASPOSE_ASSERT_EQ(certificateHolder, digitalSignatureDetails->get_CertificateHolder());
ASSERT_EQ(u"Some comments", digitalSignatureDetails->get_SignOptions()->get_Comments());

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.XpsDigitalSignature.docx", saveOptions);
```

## См. также

* Class [DigitalSignatureDetails](../../digitalsignaturedetails/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
