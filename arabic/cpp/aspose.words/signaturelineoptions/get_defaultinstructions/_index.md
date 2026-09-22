---
title: "طريقة Aspose::Words::SignatureLineOptions::get_DefaultInstructions"
linktitle: "get_DefaultInstructions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::SignatureLineOptions::get_DefaultInstructions. يحصل أو يضبط قيمة تشير إلى أن التعليمات الافتراضية تُظهر في مربع حوار التوقيع. القيمة الافتراضية لهذه الخاصية هي true في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/signaturelineoptions/get_defaultinstructions/
---
## SignatureLineOptions::get_DefaultInstructions method


يحصل أو يعيّن قيمة تشير إلى أن التعليمات الافتراضية تُعرض في مربع حوار التوقيع. القيمة الافتراضية لهذه الخاصية هي **true**.

```cpp
bool Aspose::Words::SignatureLineOptions::get_DefaultInstructions() const
```


## أمثلة



يعرض كيفية توقيع مستند باستخدام شهادة شخصية وسطر توقيع.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto signatureLineOptions = System::MakeObject<Aspose::Words::SignatureLineOptions>();
signatureLineOptions->set_Signer(u"vderyushev");
signatureLineOptions->set_SignerTitle(u"QA");
signatureLineOptions->set_Email(u"vderyushev@aspose.com");
signatureLineOptions->set_ShowDate(true);
signatureLineOptions->set_DefaultInstructions(false);
signatureLineOptions->set_Instructions(u"Please sign here.");
signatureLineOptions->set_AllowComments(true);

System::SharedPtr<Aspose::Words::Drawing::SignatureLine> signatureLine = builder->InsertSignatureLine(signatureLineOptions)->get_SignatureLine();
signatureLine->set_ProviderId(System::Guid::Parse(u"CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2"));

ASSERT_FALSE(signatureLine->get_IsSigned());
ASSERT_FALSE(signatureLine->get_IsValid());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.docx");

auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignatureLineId(signatureLine->get_Id());
signOptions->set_ProviderId(signatureLine->get_ProviderId());
signOptions->set_Comments(u"Document was signed by vderyushev");
signOptions->set_SignTime(System::DateTime::get_Now());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.docx", get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// أعد فتح المستند المحفوظ، وتحقق من أن خاصيتي "IsSigned" و "IsValid" كلاهما يساوي "true",
// مما يشير إلى أن سطر التوقيع يحتوي على توقيع.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
signatureLine = shape->get_SignatureLine();

ASSERT_TRUE(signatureLine->get_IsSigned());
ASSERT_TRUE(signatureLine->get_IsValid());
```

## انظر أيضًا

* Class [SignatureLineOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
