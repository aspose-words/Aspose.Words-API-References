---
title: get_DefaultInstructions
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value indicating that default instructions is shown in the Sign dialog. Default value for this property is true.
type: docs
weight: 27
url: /cpp/aspose.words/signaturelineoptions/get_defaultinstructions/
---
## SignatureLineOptions.get_DefaultInstructions method


Gets or sets a value indicating that default instructions is shown in the Sign dialog. Default value for this property is **true**.

```cpp
bool Aspose::Words::SignatureLineOptions::get_DefaultInstructions() const
```


## Examples




Shows how to sign a document with a personal certificate and a signature line. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

auto signatureLineOptions = MakeObject<SignatureLineOptions>();
signatureLineOptions->set_Signer(u"vderyushev");
signatureLineOptions->set_SignerTitle(u"QA");
signatureLineOptions->set_Email(u"vderyushev@aspose.com");
signatureLineOptions->set_ShowDate(true);
signatureLineOptions->set_DefaultInstructions(false);
signatureLineOptions->set_Instructions(u"Please sign here.");
signatureLineOptions->set_AllowComments(true);

SharedPtr<SignatureLine> signatureLine = builder->InsertSignatureLine(signatureLineOptions)->get_SignatureLine();
signatureLine->set_ProviderId(System::Guid::Parse(u"CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2"));

ASSERT_FALSE(signatureLine->get_IsSigned());
ASSERT_FALSE(signatureLine->get_IsValid());

doc->Save(ArtifactsDir + u"DocumentBuilder.SignatureLineProviderId.docx");

auto signOptions = MakeObject<SignOptions>();
signOptions->set_SignatureLineId(signatureLine->get_Id());
signOptions->set_ProviderId(signatureLine->get_ProviderId());
signOptions->set_Comments(u"Document was signed by vderyushev");
signOptions->set_SignTime(System::DateTime::get_Now());

SharedPtr<CertificateHolder> certHolder = CertificateHolder::Create(MyDir + u"morzal.pfx", u"aw");

DigitalSignatureUtil::Sign(ArtifactsDir + u"DocumentBuilder.SignatureLineProviderId.docx",
                           ArtifactsDir + u"DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// Re-open our saved document, and verify that the "IsSigned" and "IsValid" properties both equal "true",
// indicating that the signature line contains a signature.
doc = MakeObject<Document>(ArtifactsDir + u"DocumentBuilder.SignatureLineProviderId.Signed.docx");
auto shape = System::DynamicCast<Shape>(doc->GetChild(NodeType::Shape, 0, true));
signatureLine = shape->get_SignatureLine();

ASSERT_TRUE(signatureLine->get_IsSigned());
ASSERT_TRUE(signatureLine->get_IsValid());
```

