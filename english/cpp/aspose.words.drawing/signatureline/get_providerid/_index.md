---
title: Aspose::Words::Drawing::SignatureLine::get_ProviderId method
linktitle: get_ProviderId
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::SignatureLine::get_ProviderId method. Gets or sets signature provider identifier for this signature line. Default value is "{00000000-0000-0000-0000-000000000000}" in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.drawing/signatureline/get_providerid/
---
## SignatureLine::get_ProviderId method


Gets or sets signature provider identifier for this signature line. Default value is "{00000000-0000-0000-0000-000000000000}".

```cpp
System::Guid Aspose::Words::Drawing::SignatureLine::get_ProviderId()
```

## Remarks


The cryptographic service provider (CSP) is an independent software module that actually performs cryptography algorithms for authentication, encoding, and encryption. MS Office reserves the value of {00000000-0000-0000-0000-000000000000} for its default signature provider.

The GUID of the additionally installed provider should be obtained from the documentation shipped with the provider.

In addition, all the installed cryptographic providers are enumerated in windows registry. It can be found in the following path: HKLM\SOFTWARE\**Microsoft**\Cryptography\Defaults\Provider. There is a key name "CP Service UUID" which corresponds to a GUID of signature provider.

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
auto shape = System::ExplicitCast<Shape>(doc->GetChild(NodeType::Shape, 0, true));
signatureLine = shape->get_SignatureLine();

ASSERT_TRUE(signatureLine->get_IsSigned());
ASSERT_TRUE(signatureLine->get_IsValid());
```

## See Also

* Class [SignatureLine](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
