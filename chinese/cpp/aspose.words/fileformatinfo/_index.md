---
title: "Aspose::Words::FileFormatInfo 类"
linktitle: "FileFormatInfo"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::FileFormatInfo 类。包含由 FileFormatUtil 文档格式检测方法返回的数据。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 27000
url: /zh/cpp/aspose.words/fileformatinfo/
---
## FileFormatInfo class


包含由 [FileFormatUtil](../fileformatutil/) 文档格式检测方法返回的数据。欲了解更多，请访问 [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/) 文档文章。

```cpp
class FileFormatInfo : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Encoding](./get_encoding/)() const | 获取检测到的编码（如果适用于当前文档格式）。目前仅对 HTML 文档检测编码。 |
| [get_HasDigitalSignature](./get_hasdigitalsignature/)() const | 如果此文档包含数字签名，则返回 **true**。此属性仅表明文档上存在数字签名，但不指示签名是否有效。 |
| [get_HasMacros](./get_hasmacros/)() const | 如果此文档包含 VBA 宏，则返回 **true**。 |
| [get_IsEncrypted](./get_isencrypted/)() const | 如果文档已加密且需要密码打开，则返回 **true**。 |
| [get_LoadFormat](./get_loadformat/)() const | 获取检测到的文档格式。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 备注


您不能直接创建此类的实例。此类的对象由 [DetectFileFormat()](../) 方法返回。

## 示例



展示如何使用 [FileFormatUtil](../fileformatutil/) 类来检测文档格式和加密。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 配置 SaveOptions 对象以加密文档
// 在保存时使用密码，然后保存文档。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// 验证文档的文件类型及其加密状态。
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```


展示如何使用 [FileFormatUtil](../fileformatutil/) 类来检测文档格式和数字签名的存在。
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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
