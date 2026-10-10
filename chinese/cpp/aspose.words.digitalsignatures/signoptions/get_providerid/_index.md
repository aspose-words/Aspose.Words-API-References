---
title: "Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId 方法"
linktitle: "get_ProviderId"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId 方法。指定签名提供程序的类 ID。默认值是空（全为零）Guid，在 C++ 中。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.digitalsignatures/signoptions/get_providerid/
---
## SignOptions::get_ProviderId method


指定签名提供程序的类 ID。默认值为 **Empty (all zeroes) Guid**。

```cpp
System::Guid Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId() const
```

## 备注


加密服务提供程序 (CSP) 是一个独立的软件模块，实际执行用于身份验证、编码和加密的加密算法。MS Office 为其默认签名提供程序保留值 {00000000-0000-0000-0000-000000000000}。

额外安装的提供程序的 GUID 应从随提供程序一起提供的文档中获取。

此外，所有已安装的加密提供程序都列在 Windows 注册表中。可以在以下路径找到：HKLM\SOFTWARE\**Microsoft**\Cryptography\Defaults\Provider。该路径下有一个键名 "CP Service UUID"，对应签名提供程序的 GUID。

## 示例



展示如何使用个人证书和签名行对文档进行签署。
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

// 重新打开我们保存的文档，并验证 \"IsSigned\" 和 \"IsValid\" 属性均等于 \"true\",
// 这表明签名行包含签名。
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
signatureLine = shape->get_SignatureLine();

ASSERT_TRUE(signatureLine->get_IsSigned());
ASSERT_TRUE(signatureLine->get_IsValid());
```

## 另见

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
