---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil 类"
linktitle: "DigitalSignatureUtil"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil 类。提供用于签署文档的方法。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class


提供对文档签名的方法。要了解更多信息，请访问 [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) 文档文章。

```cpp
class DigitalSignatureUtil
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [DigitalSignatureUtil](./digitalsignatureutil/)() |  |
| static [LoadSignatures](./loadsignatures/)(const System::String\&) | 从文档加载数字签名。 |
| static [LoadSignatures](./loadsignatures/)(const System::SharedPtr\<System::IO::Stream\>\&) | 使用流从文档加载数字签名。 |
| static [LoadSignatures](./loadsignatures/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [RemoveAllSignatures](./removeallsignatures/)(const System::String\&, const System::String\&) | 从源文件中移除所有数字签名并将未签名文件写入目标文件。以下格式兼容数字签名移除：[Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/)。 |
| static [RemoveAllSignatures](./removeallsignatures/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | 从源流中的文档中移除所有数字签名并将未签名文档写入目标流。**Output will be written to the start of stream and stream size will be updated with content length.**以下格式兼容数字签名移除：[Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/)。 |
| static [RemoveAllSignatures](./removeallsignatures/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Sign](./sign/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | 使用给定的 [CertificateHolder](../certificateholder/) 和 [SignOptions](../signoptions/) 对源文档进行数字签名，并将已签名文档写入目标流。支持的格式有：[Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/)。**Output will be written to the start of stream and stream size will be updated with content length.** |
| static [Sign](./sign/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | 使用给定的 [CertificateHolder](../certificateholder/) 和 [SignOptions](../signoptions/) 对源文档进行数字签名，并将已签名文档写入目标文件。支持的格式有：[Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/)。 |
| static [Sign](./sign/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | 使用给定的 [CertificateHolder](../certificateholder/) 对源文档进行数字签名，并将已签名文档写入目标流。支持的格式有：[Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/)。**Output will be written to the start of stream and stream size will be updated with content length.** |
| static [Sign](./sign/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | 使用给定的 [CertificateHolder](../certificateholder/) 对源文档进行数字签名，并将已签名文档写入目标文件。支持的格式有：[Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/)。 |
| static [Sign](./sign/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>, System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>) |  |
| static [Sign](./sign/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>) |  |
## 备注


由于数字签名是基于文件内容而非 [Document](../../aspose.words/document/) 对象模型，这些方法被放入单独的类中。

支持的格式有：[Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/)。

## 示例



展示如何从数字签名文档中加载签名。
```cpp
// 使用 DigitalSignatureUtil 类加载已签名文档的数字签名集合有两种方式。
// 1 -  从本地文件系统的文件名加载文档：
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_MyDir() + u"Digitally signed.docx");

// 如果此集合非空，则可以验证文档已进行数字签名。
ASSERT_EQ(1, digitalSignatures->get_Count());

// 2 -  从 FileStream 加载文档：
{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Digitally signed.docx", System::IO::FileMode::Open);
    digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(stream);
    ASSERT_EQ(1, digitalSignatures->get_Count());
}
```


展示如何从数字签名文档中移除数字签名。
```cpp
// 使用 DigitalSignatureUtil 类移除数字签名有两种方式
// 通过在本地文件系统的其他位置保存未签名的副本来从已签名文档中移除签名。
// 1 - 通过文件名字符串确定已签名文档和未签名副本的位置：
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(get_MyDir() + u"Digitally signed.docx", get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - 通过文件流确定已签名文档和未签名副本的位置：
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Digitally signed.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromStream.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(streamIn, streamOut);
    }
}

// 验证我们的两个输出文档均未包含数字签名。
ASSERT_EQ(0, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromString.docx")->get_Count());
ASSERT_EQ(0, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromStream.docx")->get_Count());
```

## 另见

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
