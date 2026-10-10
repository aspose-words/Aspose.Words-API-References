---
title: "Aspose::Words::DigitalSignatures::SignOptions 类"
linktitle: "SignOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DigitalSignatures::SignOptions 类。允许指定文档签名的选项。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class


允许为文档签名指定选项。欲了解更多，请访问[数字签名使用指南](https://docs.aspose.com/words/cpp/working-with-digital-signatures/)文档文章。

```cpp
class SignOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_ApplicationVersion](./get_applicationversion/)() const | 获取或设置数字签名的应用程序版本。默认值为 "12.0"。 |
| [get_ColorDepth](./get_colordepth/)() const | 获取或设置数字签名的颜色深度。默认值为 32。 |
| [get_Comments](./get_comments/)() const | 指定数字签名的注释。默认值为 **empty string**。 |
| [get_DecryptionPassword](./get_decryptionpassword/)() const | 用于解密源文档的密码。默认值为 **empty string**。 |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | 获取或设置数字签名的水平分辨率。默认值为 1920。 |
| [get_OfficeVersion](./get_officeversion/)() const | 获取或设置数字签名的 Office 版本。默认值为 "12.0"。 |
| [get_ProviderId](./get_providerid/)() const | 指定签名提供程序的类 ID。默认值为 **Empty (all zeroes) Guid**。 |
| [get_SignatureLineId](./get_signaturelineid/)() const | 签名行标识符。默认值为 **Empty (all zeroes) Guid**。 |
| [get_SignatureLineImage](./get_signaturelineimage/)() const | 将在关联的 [SignatureLine](../../aspose.words.drawing/signatureline/) 中显示的图像。默认值为 **null**。 |
| [get_SignTime](./get_signtime/)() const | 签名日期。默认值为 **current time** (**Now**) |
| [get_VerticalResolution](./get_verticalresolution/)() const | 获取或设置数字签名的垂直分辨率。默认值为 1200。 |
| [get_WindowsVersion](./get_windowsversion/)() const | 获取或设置数字签名的 Windows 版本。默认值为 "6.1"。 |
| [get_XmlDsigLevel](./get_xmldsiglevel/)() const | 指定基于 XML-DSig 标准的数字签名级别。默认值为 [XmlDSig](../xmldsiglevel/)。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ApplicationVersion](./set_applicationversion/)(const System::String\&) | 用于 [Aspose::Words::DigitalSignatures::SignOptions::get_ApplicationVersion](./get_applicationversion/) 的设置器。 |
| [set_ColorDepth](./set_colordepth/)(int32_t) | 用于 [Aspose::Words::DigitalSignatures::SignOptions::get_ColorDepth](./get_colordepth/) 的设置器。 |
| [set_Comments](./set_comments/)(const System::String\&) | 用于 [Aspose::Words::DigitalSignatures::SignOptions::get_Comments](./get_comments/) 的设置器。 |
| [set_DecryptionPassword](./set_decryptionpassword/)(const System::String\&) | 用于 [Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword](./get_decryptionpassword/) 的设置器。 |
| [set_HorizontalResolution](./set_horizontalresolution/)(int32_t) | 用于 [Aspose::Words::DigitalSignatures::SignOptions::get_HorizontalResolution](./get_horizontalresolution/) 的设置器。 |
| [set_OfficeVersion](./set_officeversion/)(const System::String\&) | 用于 [Aspose::Words::DigitalSignatures::SignOptions::get_OfficeVersion](./get_officeversion/) 的设置器。 |
| [set_ProviderId](./set_providerid/)(System::Guid) | 用于 [Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId](./get_providerid/) 的设置器。 |
| [set_SignatureLineId](./set_signaturelineid/)(System::Guid) | 签名行标识符。默认值为 **Empty (all zeroes) Guid**。 |
| [set_SignatureLineImage](./set_signaturelineimage/)(const System::ArrayPtr\<uint8_t\>\&) | 将在关联的 [SignatureLine](../../aspose.words.drawing/signatureline/) 中显示的图像。默认值为 **null**。 |
| [set_SignTime](./set_signtime/)(System::DateTime) | 用于 [Aspose::Words::DigitalSignatures::SignOptions::get_SignTime](./get_signtime/) 的设置器。 |
| [set_VerticalResolution](./set_verticalresolution/)(int32_t) | 用于 [Aspose::Words::DigitalSignatures::SignOptions::get_VerticalResolution](./get_verticalresolution/) 的设置器。 |
| [set_WindowsVersion](./set_windowsversion/)(const System::String\&) | 用于 [Aspose::Words::DigitalSignatures::SignOptions::get_WindowsVersion](./get_windowsversion/) 的设置器。 |
| [set_XmlDsigLevel](./set_xmldsiglevel/)(Aspose::Words::DigitalSignatures::XmlDsigLevel) | 用于设置 [Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel](./get_xmldsiglevel/) 的 setter。 |
| [SignOptions](./signoptions/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
