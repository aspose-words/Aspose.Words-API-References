---
title: "Aspose::Words::DigitalSignatures::CertificateHolder::get_Certificate 方法"
linktitle: "get_Certificate"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DigitalSignatures::CertificateHolder::get_Certificate 方法。返回在 C++ 中持有私钥、公共密钥和证书链的 X509Certificate2 实例。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.digitalsignatures/certificateholder/get_certificate/
---
## CertificateHolder::get_Certificate method


返回持有私钥、公共密钥和证书链的 **X509Certificate2** 实例。

```cpp
System::SharedPtr<System::Security::Cryptography::X509Certificates::X509Certificate2> Aspose::Words::DigitalSignatures::CertificateHolder::get_Certificate()
```


### ReturnValue

**X509Certificate2****X509Certificate2** instance

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

* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
