---
title: "Aspose::Words::SignatureLineOptions 类"
linktitle: "SignatureLineOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::SignatureLineOptions 类。允许指定插入签名行的选项。用于 DocumentBuilder。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 61000
url: /zh/cpp/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class


允许指定插入签名行的选项。用于 [DocumentBuilder](../documentbuilder/)。要了解更多，请访问 [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) 文档文章。

```cpp
class SignatureLineOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() const | 获取或设置一个值，指示签署人在签名对话框中是否可以添加评论。此属性的默认值为 **false**。 |
| [get_DefaultInstructions](./get_defaultinstructions/)() const | 获取或设置一个值，指示在签名对话框中是否显示默认说明。此属性的默认值为 **true**。 |
| [get_Email](./get_email/)() const | 获取或设置建议的签署人电子邮件地址。此属性的默认值为 **empty string**。 |
| [get_Instructions](./get_instructions/)() const | 获取或设置在签署签名行时显示给签署人的说明。此属性的默认值为 **empty string**。 |
| [get_ShowDate](./get_showdate/)() const | 获取或设置一个值，指示签名行中是否显示签署日期。此属性的默认值为 **true**。 |
| [get_Signer](./get_signer/)() const | 获取签名行的建议签署人。此属性的默认值为 **empty string**。 |
| [get_SignerTitle](./get_signertitle/)() const | 获取建议签署人的职称。此属性的默认值为 **empty string**。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | 用于 [Aspose::Words::SignatureLineOptions::get_AllowComments](./get_allowcomments/) 的设置器。 |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | 用于 [Aspose::Words::SignatureLineOptions::get_DefaultInstructions](./get_defaultinstructions/) 的设置器。 |
| [set_Email](./set_email/)(const System::String\&) | 用于 [Aspose::Words::SignatureLineOptions::get_Email](./get_email/) 的设置器。 |
| [set_Instructions](./set_instructions/)(const System::String\&) | 用于 [Aspose::Words::SignatureLineOptions::get_Instructions](./get_instructions/) 的设置器。 |
| [set_ShowDate](./set_showdate/)(bool) | 用于 [Aspose::Words::SignatureLineOptions::get_ShowDate](./get_showdate/) 的设置器。 |
| [set_Signer](./set_signer/)(const System::String\&) | 设置签名行的建议签署人。此属性的默认值为 **empty string**。 |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | 设置建议的签署人职称。此属性的默认值为 **empty string**。 |
| [SignatureLineOptions](./signaturelineoptions/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
