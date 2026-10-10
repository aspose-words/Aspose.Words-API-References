---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureType enum"
linktitle: "DigitalSignatureType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureType 枚举。指定 C++ 中数字签名的类型。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.digitalsignatures/digitalsignaturetype/
---
## DigitalSignatureType enum


指定数字签名的类型。

```cpp
enum class DigitalSignatureType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 未知 | 0 | 指示错误，未知的数字签名类型。 |
| CryptoApi | 1 | 在 Microsoft Word 97-2003 .DOC 二进制文档中使用的 Crypto API 签名方法。 |
| XmlDsig | 2 | 在 OOXML 和 OpenDocument 文档中使用的 XmlDsig 签名方法。 |


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

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
