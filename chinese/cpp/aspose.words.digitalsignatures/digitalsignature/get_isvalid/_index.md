---
title: "Aspose::Words::DigitalSignatures::DigitalSignature::get_IsValid 方法"
linktitle: "get_IsValid"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DigitalSignatures::DigitalSignature::get_IsValid 方法。若此数字签名有效且文档未被篡改，则返回 true（C++）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.digitalsignatures/digitalsignature/get_isvalid/
---
## DigitalSignature::get_IsValid method


如果此数字签名有效且文档未被篡改，则返回 **true**。

```cpp
bool Aspose::Words::DigitalSignatures::DigitalSignature::get_IsValid() const
```


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

* Class [DigitalSignature](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
