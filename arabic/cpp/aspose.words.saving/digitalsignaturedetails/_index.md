---
title: "الفئة Aspose::Words::Saving::DigitalSignatureDetails"
linktitle: "DigitalSignatureDetails"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Saving::DigitalSignatureDetails. تحتوي على تفاصيل لتوقيع مستند باستخدام توقيع رقمي في C++."
type: docs
weight: 2500
url: /ar/cpp/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class


يحتوي على تفاصيل توقيع المستند باستخدام توقيع رقمي.

```cpp
class DigitalSignatureDetails : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [DigitalSignatureDetails](./digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | يُنشئ مثيلًا جديدًا من الفئة [DigitalSignatureDetails](./). |
| [get_CertificateHolder](./get_certificateholder/)() const | يحصل أو يعيّن كائنًا من نوع [CertificateHolder](./get_certificateholder/) يحتوي على الشهادة المستخدمة لتوقيع المستند. |
| [get_SignOptions](./get_signoptions/)() const | يحصل أو يعيّن كائنًا من نوع [SignOptions](./get_signoptions/) يُستخدم لتوقيع المستند. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | دالة تعيين لـ [Aspose::Words::Saving::DigitalSignatureDetails::get_CertificateHolder](./get_certificateholder/). |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | دالة تعيين لـ [Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions](./get_signoptions/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
