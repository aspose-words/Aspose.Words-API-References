---
title: "Aspose::Words::Saving::DigitalSignatureDetails::DigitalSignatureDetails منشئ"
linktitle: "DigitalSignatureDetails"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::DigitalSignatureDetails::DigitalSignatureDetails منشئ. يهيئ مثيلًا جديدًا من فئة DigitalSignatureDetails في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.saving/digitalsignaturedetails/digitalsignaturedetails/
---
## DigitalSignatureDetails::DigitalSignatureDetails constructor


يهيئ مثيلًا جديدًا من فئة [DigitalSignatureDetails](../)

```cpp
Aspose::Words::Saving::DigitalSignatureDetails::DigitalSignatureDetails(const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certificateHolder, const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> &signOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| certificateHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | حامل شهادة يحتوي على الشهادة نفسها. |
| signOptions | const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\& | خيارات التوقيع لاستخدامها في توقيع مستند. |

## أمثلة



يعرض كيفية توقيع مستند OOXML.
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

## انظر أيضًا

* Class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* Class [SignOptions](../../../aspose.words.digitalsignatures/signoptions/)
* Class [DigitalSignatureDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
