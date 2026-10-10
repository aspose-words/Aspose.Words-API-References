---
title: "Aspose::Words::DigitalSignatures::CertificateHolder::Create 方法"
linktitle: "Create"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DigitalSignatures::CertificateHolder::Create 方法。使用 PKCS12 存储的字节数组及其密码在 C++ 中创建 CertificateHolder 对象。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.digitalsignatures/certificateholder/create/
---
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) method


使用 PKCS12 存储的字节数组及其密码创建 [CertificateHolder](../) 对象。

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::SharedPtr<System::Security::SecureString> &password)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | 包含 X.509 证书数据的字节数组。 |
| 密码 | const System::SharedPtr\<System::Security::SecureString\>\& | 访问 X.509 证书数据所需的密码。 |

### ReturnValue

[CertificateHolder](../) 的实例

## 另见

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) method


使用 PKCS12 存储的字节数组及其密码创建 [CertificateHolder](../) 对象。

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::String &password)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | 包含 X.509 证书数据的字节数组。 |
| 密码 | const System::String\& | 访问 X.509 证书数据所需的密码。 |

### ReturnValue

[CertificateHolder](../) 的实例

## 另见

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&) method


使用 PKCS12 存储的路径及其密码创建 [CertificateHolder](../) 对象。

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文件名 | const System::String\& | 证书文件的名称。 |
| 密码 | const System::String\& | 访问 X.509 证书数据所需的密码。 |

### ReturnValue

[CertificateHolder](../) 的实例

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

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&, const System::String\&) method


使用 PKCS12 存储的路径、其密码以及用于查找私钥和证书的别名创建 [CertificateHolder](../) 对象。

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password, const System::String &alias)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文件名 | const System::String\& | 证书文件的名称。 |
| 密码 | const System::String\& | 访问 X.509 证书数据所需的密码。 |
| alias | const System::String\& | 证书及其私钥的关联别名 |

### ReturnValue

[CertificateHolder](../) 的实例

## 另见

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
