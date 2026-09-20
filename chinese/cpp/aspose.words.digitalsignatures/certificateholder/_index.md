---
title: "Aspose::Words::DigitalSignatures::CertificateHolder class"
linktitle: "CertificateHolder"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DigitalSignatures::CertificateHolder 类。表示 X509Certificate2 实例的持有者。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class


表示 **X509Certificate2** 实例的持有者。要了解更多信息，请访问 [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) 文档文章。

```cpp
class CertificateHolder : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) | 使用 PKCS12 存储的字节数组及其密码创建 [CertificateHolder](./) 对象。 |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) | 使用 PKCS12 存储的字节数组及其密码创建 [CertificateHolder](./) 对象。 |
| static [Create](./create/)(const System::String\&, const System::String\&) | 使用 PKCS12 存储的路径及其密码创建 [CertificateHolder](./) 对象。 |
| static [Create](./create/)(const System::String\&, const System::String\&, const System::String\&) | 使用 PKCS12 存储的路径、密码以及用于查找私钥和证书的别名创建 [CertificateHolder](./) 对象。 |
| [get_Certificate](./get_certificate/)() | 返回持有私钥、公共密钥和证书链的 **X509Certificate2** 实例。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 备注


[CertificateHolder](./) can be created by static factory methods only. It contains an instance of **X509Certificate2** which is used to introduce private, public keys and certificate chains into the system. This class is applied in [DigitalSignatureUtil](../digitalsignatureutil/) and [PdfDigitalSignatureDetails](../../aspose.words.saving/pdfdigitalsignaturedetails/) instead of obsolete methods with **X509Certificate2** as parameters.

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


展示如何对加密文档文件进行签名。
```cpp
// 从包含私钥的 PKCS#12 存储创建 X.509 证书。
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// 创建将在新数字签名中使用的注释、日期和解密密码。
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

// 为未签名的输入文档设置本地系统文件名，并为其新的数字签名副本设置输出文件名。
System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.DecryptionPassword.docx";

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## 另见

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
