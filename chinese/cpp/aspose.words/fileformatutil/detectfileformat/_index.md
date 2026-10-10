---
title: "Aspose::Words::FileFormatUtil::DetectFileFormat 方法"
linktitle: "DetectFileFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::FileFormatUtil::DetectFileFormat 方法。检测并返回存储在流中的文档格式信息（C++）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/fileformatutil/detectfileformat/
---
## FileFormatUtil::DetectFileFormat(const System::SharedPtr\<System::IO::Stream\>\&) method


检测并返回存储在流中的文档格式信息。

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::SharedPtr<System::IO::Stream> &stream)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 流 | const System::SharedPtr\<System::IO::Stream\>\& | 该流。 |

### ReturnValue

一个包含检测信息的 [FileFormatInfo](../../fileformatinfo/) 对象。
## 备注


流必须定位在文档的开头。

当此方法返回时，流中的位置会恢复到原始位置。

即使此方法检测到文档格式，也不能保证指定的文档是有效的。此方法仅通过读取足以进行检测的数据来检测文档格式。要完整验证文档的有效性，需要将文档加载到 [Document](../../document/) 对象中。

当识别出格式但由于损坏导致检测无法完成时，此方法会抛出 [FileCorruptedException](../../filecorruptedexception/)。

## 示例



展示如何使用 [FileFormatUtil](../) 方法检测文档的格式。
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

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(const System::String\&) method


检测并返回存储在磁盘文件中的文档格式信息。

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::String &fileName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文件名 | const System::String\& | 文件名。 |

### ReturnValue

一个包含检测信息的 [FileFormatInfo](../../fileformatinfo/) 对象。
## 备注


即使此方法检测到文档格式，也不能保证指定的文档是有效的。此方法仅通过读取足以进行检测的数据来检测文档格式。要完整验证文档的有效性，需要将文档加载到 [Document](../../document/) 对象中。

当识别出格式但由于损坏导致检测无法完成时，此方法会抛出 [FileCorruptedException](../../filecorruptedexception/)。

## 示例



展示如何使用 [FileFormatUtil](../) 类来检测文档格式和加密。
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


展示如何使用 [FileFormatUtil](../) 类来检测文档格式以及数字签名的存在。
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

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(std::basic_istream<CharType, Traits> &stream)
```

## 另见

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
