---
title: "Aspose::Words::FileFormatInfo::get_HasDigitalSignature 方法"
linktitle: "get_HasDigitalSignature"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::FileFormatInfo::get_HasDigitalSignature 方法。若文档包含数字签名则返回 true。此属性仅说明文档上存在数字签名，但不指示签名是否有效（C++）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/fileformatinfo/get_hasdigitalsignature/
---
## FileFormatInfo::get_HasDigitalSignature method


如果此文档包含数字签名，则返回 **true**。此属性仅表明文档上存在数字签名，但不指示签名是否有效。

```cpp
bool Aspose::Words::FileFormatInfo::get_HasDigitalSignature() const
```

## 备注


此属性用于帮助您将已数字签名的文档与未签名的文档进行分类。如果使用 Aspose.Words 修改并保存已数字签名的文档，则数字签名将会丢失。这是设计如此，因为数字签名用于保护文档的真实性。使用此属性，您可以在像处理普通文档一样处理之前检测到已数字签名的文档，并采取措施避免丢失数字签名，例如通知用户。

## 示例



展示如何使用 [FileFormatUtil](../../fileformatutil/) 类来检测文档格式和数字签名的存在。
```cpp
// 使用 FileFormatInfo 实例来验证文档未被数字签名。
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx");

ASSERT_EQ(u".docx", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_FALSE(info->get_HasDigitalSignature());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx", certificateHolder, signOptions);

// 使用新的 FileFormatInstance 来确认其已签名。
info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx");

ASSERT_TRUE(info->get_HasDigitalSignature());

// 我们可以加载并以如下方式访问已签名文档的签名集合。
ASSERT_EQ(1, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx")->get_Count());
```

## 另见

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
