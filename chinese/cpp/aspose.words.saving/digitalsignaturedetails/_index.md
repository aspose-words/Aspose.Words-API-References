---
title: "Aspose::Words::Saving::DigitalSignatureDetails 类"
linktitle: "DigitalSignatureDetails"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::DigitalSignatureDetails 类。包含在 C++ 中使用数字签名对文档进行签名的详细信息。"
type: docs
weight: 2500
url: /zh/cpp/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class


包含使用数字签名对文档进行签署的详细信息。

```cpp
class DigitalSignatureDetails : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [DigitalSignatureDetails](./digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | 初始化一个新的 [DigitalSignatureDetails](./) 类实例。 |
| [get_CertificateHolder](./get_certificateholder/)() const | 获取或设置一个包含用于签署文档的证书的 [CertificateHolder](./get_certificateholder/) 对象。 |
| [get_SignOptions](./get_signoptions/)() const | 获取或设置一个用于签署文档的 [SignOptions](./get_signoptions/) 对象。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | 用于设置 [Aspose::Words::Saving::DigitalSignatureDetails::get_CertificateHolder](./get_certificateholder/) 的 setter。 |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | 用于设置 [Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions](./get_signoptions/) 的 setter。 |
| static [Type](./type/)() |  |

## 示例



展示如何对 OOXML 文档进行签名。
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

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
