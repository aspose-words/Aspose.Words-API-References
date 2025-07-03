---
title: Aspose::Words::SignatureLineOptions class
linktitle: SignatureLineOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::SignatureLineOptions class. Allows to specify options for signature line being inserted. Used in DocumentBuilder. To learn more, visit the  documentation article in C++.'
type: docs
weight: 61000
url: /cpp/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class


Allows to specify options for signature line being inserted. Used in [DocumentBuilder](../documentbuilder/). To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) documentation article.

```cpp
class SignatureLineOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() const | Gets or sets a value indicating that the signer can add comments in the Sign dialog. Default value for this property is **false**. |
| [get_DefaultInstructions](./get_defaultinstructions/)() const | Gets or sets a value indicating that default instructions is shown in the Sign dialog. Default value for this property is **true**. |
| [get_Email](./get_email/)() const | Gets or sets suggested signer's e-mail address. Default value for this property is **empty string**. |
| [get_Instructions](./get_instructions/)() const | Gets or sets instructions to the signer that are displayed on signing the signature line. Default value for this property is **empty string**. |
| [get_ShowDate](./get_showdate/)() const | Gets or sets a value indicating that sign date is shown in the signature line. Default value for this property is **true**. |
| [get_Signer](./get_signer/)() const | Gets suggested signer of the signature line. Default value for this property is **empty string**. |
| [get_SignerTitle](./get_signertitle/)() const | Gets suggested signer's title. Default value for this property is **empty string**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | Setter for [Aspose::Words::SignatureLineOptions::get_AllowComments](./get_allowcomments/). |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | Setter for [Aspose::Words::SignatureLineOptions::get_DefaultInstructions](./get_defaultinstructions/). |
| [set_Email](./set_email/)(const System::String\&) | Setter for [Aspose::Words::SignatureLineOptions::get_Email](./get_email/). |
| [set_Instructions](./set_instructions/)(const System::String\&) | Setter for [Aspose::Words::SignatureLineOptions::get_Instructions](./get_instructions/). |
| [set_ShowDate](./set_showdate/)(bool) | Setter for [Aspose::Words::SignatureLineOptions::get_ShowDate](./get_showdate/). |
| [set_Signer](./set_signer/)(const System::String\&) | Sets suggested signer of the signature line. Default value for this property is **empty string**. |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | Sets suggested signer's title. Default value for this property is **empty string**. |
| [SignatureLineOptions](./signaturelineoptions/)() |  |
| static [Type](./type/)() |  |

## Examples



Shows how to sign a document with a personal certificate and a signature line. 
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

// Re-open our saved document, and verify that the "IsSigned" and "IsValid" properties both equal "true",
// indicating that the signature line contains a signature.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
signatureLine = shape->get_SignatureLine();

ASSERT_TRUE(signatureLine->get_IsSigned());
ASSERT_TRUE(signatureLine->get_IsValid());
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
