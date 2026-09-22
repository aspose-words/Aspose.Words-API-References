---
title: "Aspose::Words::SignatureLineOptions class"
linktitle: "SignatureLineOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::SignatureLineOptions class. يسمح بتحديد خيارات سطر التوقيع الذي يتم إدراجه. يُستخدم في DocumentBuilder. لمزيد من المعلومات، زر مقالة الوثائق في C++."
type: docs
weight: 61000
url: /ar/cpp/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class


يسمح بتحديد خيارات سطر التوقيع الذي يتم إدراجه. يُستخدم في [DocumentBuilder](../documentbuilder/). لمزيد من المعلومات، زر مقالة الوثائق [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class SignatureLineOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() const | يحصل أو يعيّن قيمة تشير إلى أن الموقّع يمكنه إضافة تعليقات في مربع حوار التوقيع. القيمة الافتراضية لهذه الخاصية هي **false** |
| [get_DefaultInstructions](./get_defaultinstructions/)() const | يحصل أو يعيّن قيمة تشير إلى أن التعليمات الافتراضية تُعرض في مربع حوار التوقيع. القيمة الافتراضية لهذه الخاصية هي **true**. |
| [get_Email](./get_email/)() const | يحصل أو يعيّن عنوان البريد الإلكتروني المقترح للموقّع. القيمة الافتراضية لهذه الخاصية هي **empty string**. |
| [get_Instructions](./get_instructions/)() const | يحصل أو يعيّن التعليمات للموقّع التي تُعرض عند توقيع سطر التوقيع. القيمة الافتراضية لهذه الخاصية هي **empty string**. |
| [get_ShowDate](./get_showdate/)() const | يحصل أو يعيّن قيمة تشير إلى أن تاريخ التوقيع يُعرض في سطر التوقيع. القيمة الافتراضية لهذه الخاصية هي **true**. |
| [get_Signer](./get_signer/)() const | يحصل على الموقّع المقترح لسطر التوقيع. القيمة الافتراضية لهذه الخاصية هي **empty string**. |
| [get_SignerTitle](./get_signertitle/)() const | يحصل على لقب الموقّع المقترح. القيمة الافتراضية لهذه الخاصية هي **empty string**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | مُعيّن لـ [Aspose::Words::SignatureLineOptions::get_AllowComments](./get_allowcomments/). |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | مُعيّن لـ [Aspose::Words::SignatureLineOptions::get_DefaultInstructions](./get_defaultinstructions/). |
| [set_Email](./set_email/)(const System::String\&) | مُعيّن لـ [Aspose::Words::SignatureLineOptions::get_Email](./get_email/). |
| [set_Instructions](./set_instructions/)(const System::String\&) | مُعيّن لـ [Aspose::Words::SignatureLineOptions::get_Instructions](./get_instructions/). |
| [set_ShowDate](./set_showdate/)(bool) | مُعيّن لـ [Aspose::Words::SignatureLineOptions::get_ShowDate](./get_showdate/). |
| [set_Signer](./set_signer/)(const System::String\&) | يعيّن الموقّع المقترح لسطر التوقيع. القيمة الافتراضية لهذه الخاصية هي **empty string**. |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | يعيّن لقب الموقّع المقترح. القيمة الافتراضية لهذه الخاصية هي **empty string**. |
| [SignatureLineOptions](./signaturelineoptions/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
