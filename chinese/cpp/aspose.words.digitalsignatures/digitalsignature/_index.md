---
title: "Aspose::Words::DigitalSignatures::DigitalSignature 类"
linktitle: "DigitalSignature"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DigitalSignatures::DigitalSignature 类。表示文档上的数字签名及其验证结果。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class


表示文档上的数字签名及其验证结果。要了解更多信息，请访问 [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) 文档文章。

```cpp
class DigitalSignature : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_ApplicationVersion](./get_applicationversion/)() | 获取数字签名的应用程序版本。 |
| [get_CertificateHolder](./get_certificateholder/)() const | 返回包含用于签署文档的证书的证书持有者对象。 |
| [get_ColorDepth](./get_colordepth/)() | 获取数字签名的颜色深度。 |
| [get_Comments](./get_comments/)() | 获取签名用途注释。 |
| [get_HorizontalResolution](./get_horizontalresolution/)() | 获取数字签名的水平分辨率。 |
| [get_IssuerName](./get_issuername/)() | 返回证书颁发者的主题可辨识名称。 |
| [get_IsValid](./get_isvalid/)() const | 如果此数字签名有效且文档未被篡改，则返回 **true**。 |
| [get_OfficeVersion](./get_officeversion/)() | 获取数字签名的 Office 版本。 |
| [get_SignatureType](./get_signaturetype/)() const | 获取数字签名的类型。 |
| [get_SignatureValue](./get_signaturevalue/)() const | 获取表示签名值的字节数组。 |
| [get_SignTime](./get_signtime/)() const | 获取文档签署的时间。 |
| [get_SubjectName](./get_subjectname/)() | 返回用于签署文档的证书的主题可辨识名称。 |
| [get_VerticalResolution](./get_verticalresolution/)() | 获取数字签名的垂直分辨率。 |
| [get_WindowsVersion](./get_windowsversion/)() | 获取数字签名的 Windows 版本。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | 返回一个用户友好的字符串，显示此对象的值。 |
| static [Type](./type/)() |  |

## 示例



展示如何验证并显示文档中每个签名的信息。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Digitally signed.docx");

for (auto&& signature : doc->get_DigitalSignatures())
{
    std::cout << System::String::Format(u"{0} signature: ", (signature->get_IsValid() ? System::String(u"Valid") : System::String(u"Invalid"))) << std::endl;
    std::cout << System::String::Format(u"\tReason:\t{0}", signature->get_Comments()) << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", signature->get_SignatureType()) << std::endl;
    std::cout << System::String::Format(u"\tSign time:\t{0}", signature->get_SignTime()) << std::endl;
    std::cout << System::String::Format(u"\tSubject name:\t{0}", signature->get_CertificateHolder()->get_Certificate()->get_SubjectName()) << std::endl;
    std::cout << System::String::Format(u"\tIssuer name:\t{0}", signature->get_CertificateHolder()->get_Certificate()->get_IssuerName()->get_Name()) << std::endl;
    std::cout << std::endl;
}
```

## 另见

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
