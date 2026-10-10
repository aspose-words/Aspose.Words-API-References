---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures 方法"
linktitle: "RemoveAllSignatures"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures 方法。 从源流中的文档中移除所有数字签名，并将未签名的文档写入目标流。 输出将写入流的起始位置，流大小将根据内容长度更新。以下格式兼容数字签名移除：Doc、Dot、Docx、Dotx、Docm、Dotm、Odt、Ott（C++）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## DigitalSignatureUtil::RemoveAllSignatures(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


从源流中的文档中移除所有数字签名，并将未签名的文档写入目标流。 **输出将写入流的起始位置，流大小将根据内容长度更新。**以下格式兼容数字签名移除： [Doc](../../../aspose.words/loadformat/)、[Dot](../../../aspose.words/loadformat/)、[Docx](../../../aspose.words/loadformat/)、[Dotx](../../../aspose.words/loadformat/)、[Docm](../../../aspose.words/loadformat/)、[Dotm](../../../aspose.words/loadformat/)、[Odt](../../../aspose.words/loadformat/)、[Ott](../../../aspose.words/loadformat/)。

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(const System::SharedPtr<System::IO::Stream> &srcStream, const System::SharedPtr<System::IO::Stream> &dstStream)
```


## 示例



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

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::RemoveAllSignatures(const System::String\&, const System::String\&) method


从源文件中移除所有数字签名，并将未签名的文件写入目标文件。以下格式兼容数字签名移除： [Doc](../../../aspose.words/loadformat/)、[Dot](../../../aspose.words/loadformat/)、[Docx](../../../aspose.words/loadformat/)、[Dotx](../../../aspose.words/loadformat/)、[Docm](../../../aspose.words/loadformat/)、[Dotm](../../../aspose.words/loadformat/)、[Odt](../../../aspose.words/loadformat/)、[Ott](../../../aspose.words/loadformat/)。

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(const System::String &srcFileName, const System::String &dstFileName)
```


## 示例



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

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::RemoveAllSignatures(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(std::basic_istream<CharType, Traits> &srcStream, std::basic_ostream<CharType, Traits> &dstStream)
```

## 另见

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
