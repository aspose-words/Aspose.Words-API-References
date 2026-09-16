---
title: "Aspose::Words::FileFormatInfo::get_LoadFormat 方法"
linktitle: "get_LoadFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::FileFormatInfo::get_LoadFormat 方法。获取在 C++ 中检测到的文档格式。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/fileformatinfo/get_loadformat/
---
## FileFormatInfo::get_LoadFormat method


获取检测到的文档格式。

```cpp
Aspose::Words::LoadFormat Aspose::Words::FileFormatInfo::get_LoadFormat() const
```

## 备注


当 OOXML 文档被加密时，若不先解密则无法确定它是 Excel、Word 还是 PowerPoint 文档，因此对于加密的 OOXML 文档，此属性始终返回 [Docx](../../loadformat/)。

## 示例



展示如何使用 [FileFormatUtil](../../fileformatutil/) 类来检测文档格式和加密情况。
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


展示如何使用 [FileFormatUtil](../../fileformatutil/) 方法检测文档的格式。
```cpp
// 从缺少文件扩展名的文件加载文档，然后检测其文件格式。
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // 下面是将 LoadFormat 转换为相应 SaveFormat 的两种方法。
    // 1 - 获取 LoadFormat 的文件扩展名字符串，然后从该字符串获取相应的 SaveFormat：
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 - 直接将 LoadFormat 转换为其 SaveFormat：
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // 从流中加载文档，然后保存为自动检测的文件扩展名。
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```

## 另见

* Enum [LoadFormat](../../loadformat/)
* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
