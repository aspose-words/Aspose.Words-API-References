---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign method"
linktitle: "Sign"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign 方法。 使用给定的 CertificateHolder 对源文档进行数字签名，并将已签名的文档写入目标流。 支持的格式有：Doc、Dot、Docx、Dotx、Docm、Dotm、Odt、Ott。输出将写入流的起始位置，流大小将根据内容长度更新（C++）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## DigitalSignatureUtil::Sign(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) method


使用给定的 [CertificateHolder](../../certificateholder/) 对源文档进行数字签名，并将已签名的文档写入目标流。支持的格式有： [Doc](../../../aspose.words/loadformat/)、[Dot](../../../aspose.words/loadformat/)、[Docx](../../../aspose.words/loadformat/)、[Dotx](../../../aspose.words/loadformat/)、[Docm](../../../aspose.words/loadformat/)、[Dotm](../../../aspose.words/loadformat/)、[Odt](../../../aspose.words/loadformat/)、[Ott](../../../aspose.words/loadformat/)。**输出将写入流的起始位置，流大小将根据内容长度更新。**

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::SharedPtr<System::IO::Stream> &srcStream, const System::SharedPtr<System::IO::Stream> &dstStream, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| srcStream | const System::SharedPtr\<System::IO::Stream\>\& | 包含待签名文档的流。 |
| dstStream | const System::SharedPtr\<System::IO::Stream\>\& | 签名后文档将写入的流。 |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | [CertificateHolder](../../certificateholder/) 对象，包含用于签署文件的证书。持有者中的证书必须包含私钥。 |

## 示例



展示如何使用 X.509 证书对文档进行签名。
```cpp
// 验证文档未被签名。
ASSERT_FALSE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx")->get_HasDigitalSignature());

// 从 PKCS12 文件创建一个 CertificateHolder 对象，我们将使用它来签署文档。
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);

// 将文档的已签名副本保存到本地文件系统有两种方式：
// 1 - 通过本地系统文件名指定文档，并将已签名副本保存到另一个文件名指定的位置。
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 - 从流中获取文档，并将已签名副本保存到另一个流。
{
    auto inDoc = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 请验证文档的所有数字签名均有效并检查其详细信息。
auto signedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.DigitalSignature.docx");
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(1, digitalSignatureCollection->get_Count());
ASSERT_EQ(Aspose::Words::DigitalSignatures::DigitalSignatureType::XmlDsig, digitalSignatureCollection->idx_get(0)->get_SignatureType());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName());
```

## 另见

* Class [CertificateHolder](../../certificateholder/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) method


使用给定的 [CertificateHolder](../../certificateholder/) 和 [SignOptions](../../signoptions/) 对源文档进行数字签名，并将已签名的文档写入目标流。支持的格式有： [Doc](../../../aspose.words/loadformat/)、[Dot](../../../aspose.words/loadformat/)、[Docx](../../../aspose.words/loadformat/)、[Dotx](../../../aspose.words/loadformat/)、[Docm](../../../aspose.words/loadformat/)、[Dotm](../../../aspose.words/loadformat/)、[Odt](../../../aspose.words/loadformat/)、[Ott](../../../aspose.words/loadformat/)。**输出将写入流的起始位置，流大小将根据内容长度更新。**

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::SharedPtr<System::IO::Stream> &srcStream, const System::SharedPtr<System::IO::Stream> &dstStream, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder, const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> &signOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| srcStream | const System::SharedPtr\<System::IO::Stream\>\& | 包含待签名文档的流。 |
| dstStream | const System::SharedPtr\<System::IO::Stream\>\& | 签名后文档将写入的流。 |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | [CertificateHolder](../../certificateholder/) 对象，包含用于签署文件的证书。持有者中的证书必须包含私钥。 |
| signOptions | const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\& | [SignOptions](../../signoptions/) 对象，包含各种签名选项。 |

## 示例



展示如何对文档进行数字签名。
```cpp
// 从包含私钥的 PKCS#12 存储创建 X.509 证书。
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// 创建将在新数字签名中使用的注释和日期。
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// 通过文件流从本地文件系统获取未签名的文档，
// 然后根据输出文件流的文件名创建其签名副本。
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## 另见

* Class [CertificateHolder](../../certificateholder/)
* Class [SignOptions](../../signoptions/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) method


使用给定的 [CertificateHolder](../../certificateholder/) 对源文档进行数字签名，并将已签名的文档写入目标文件。支持的格式有： [Doc](../../../aspose.words/loadformat/)、[Dot](../../../aspose.words/loadformat/)、[Docx](../../../aspose.words/loadformat/)、[Dotx](../../../aspose.words/loadformat/)、[Docm](../../../aspose.words/loadformat/)、[Dotm](../../../aspose.words/loadformat/)、[Odt](../../../aspose.words/loadformat/)、[Ott](../../../aspose.words/loadformat/)。

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::String &srcFileName, const System::String &dstFileName, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| srcFileName | const System::String\& | 待签名文档的文件名。 |
| dstFileName | const System::String\& | 已签名文档输出的文件名。 |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | [CertificateHolder](../../certificateholder/) 对象，包含用于签署文件的证书。持有者中的证书必须包含私钥。 |

## 示例



展示如何使用 X.509 证书对文档进行签名。
```cpp
// 验证文档未被签名。
ASSERT_FALSE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx")->get_HasDigitalSignature());

// 从 PKCS12 文件创建一个 CertificateHolder 对象，我们将使用它来签署文档。
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);

// 将文档的已签名副本保存到本地文件系统有两种方式：
// 1 - 通过本地系统文件名指定文档，并将已签名副本保存到另一个文件名指定的位置。
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 - 从流中获取文档，并将已签名副本保存到另一个流。
{
    auto inDoc = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 请验证文档的所有数字签名均有效并检查其详细信息。
auto signedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.DigitalSignature.docx");
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(1, digitalSignatureCollection->get_Count());
ASSERT_EQ(Aspose::Words::DigitalSignatures::DigitalSignatureType::XmlDsig, digitalSignatureCollection->idx_get(0)->get_SignatureType());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName());
```

## 另见

* Class [CertificateHolder](../../certificateholder/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) method


使用给定的 [CertificateHolder](../../certificateholder/) 和 [SignOptions](../../signoptions/) 对源文档进行数字签名，并将已签名的文档写入目标文件。支持的格式有： [Doc](../../../aspose.words/loadformat/)、[Dot](../../../aspose.words/loadformat/)、[Docx](../../../aspose.words/loadformat/)、[Dotx](../../../aspose.words/loadformat/)、[Docm](../../../aspose.words/loadformat/)、[Dotm](../../../aspose.words/loadformat/)、[Odt](../../../aspose.words/loadformat/)、[Ott](../../../aspose.words/loadformat/)。

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::String &srcFileName, const System::String &dstFileName, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder, const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> &signOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| srcFileName | const System::String\& | 待签名文档的文件名。 |
| dstFileName | const System::String\& | 已签名文档输出的文件名。 |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | [CertificateHolder](../../certificateholder/) 对象，包含用于签署文件的证书。持有者中的证书必须包含私钥。 |
| signOptions | const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\& | [SignOptions](../../signoptions/) 对象，包含各种签名选项。 |

## 示例



展示如何使用额外的签名选项对文档进行签名。
```cpp
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_WindowsVersion(u"10.0");
signOptions->set_ApplicationVersion(u"16.0.19127");
signOptions->set_OfficeVersion(u"16.0.19127/27");
signOptions->set_HorizontalResolution(1024);
signOptions->set_VerticalResolution(768);
signOptions->set_ColorDepth(24);

System::ArrayPtr<uint8_t> certBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"morzal.pfx");
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> cert = Aspose::Words::DigitalSignatures::CertificateHolder::Create(certBytes, u"aw");
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Digitally signed.docx", get_ArtifactsDir() + u"DigitalSignatureUtil.docx", cert, signOptions);

auto signedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DigitalSignatureUtil.docx");

System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature> signature = signedDoc->get_DigitalSignatures()->idx_get(0);
ASSERT_EQ(1, signedDoc->get_DigitalSignatures()->get_Count());
ASSERT_TRUE(signature->get_IsValid());
ASSERT_EQ(u"10.0", signature->get_WindowsVersion());
ASSERT_EQ(u"16.0.19127", signature->get_ApplicationVersion());
ASSERT_EQ(u"16.0.19127/27", signature->get_OfficeVersion());
ASSERT_EQ(1024, signature->get_HorizontalResolution());
ASSERT_EQ(768, signature->get_VerticalResolution());
ASSERT_EQ(24, signature->get_ColorDepth());
```

## 另见

* Class [CertificateHolder](../../certificateholder/)
* Class [SignOptions](../../signoptions/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(std::basic_istream<CharType, Traits> &srcStream, std::basic_ostream<CharType, Traits> &dstStream, System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certHolder)
```

## 另见

* Class [CertificateHolder](../../certificateholder/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>, System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(std::basic_istream<CharType, Traits> &srcStream, std::basic_ostream<CharType, Traits> &dstStream, System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certHolder, System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> signOptions)
```

## 另见

* Class [CertificateHolder](../../certificateholder/)
* Class [SignOptions](../../signoptions/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
