---
title: "Aspose::Words::DigitalSignatures::CertificateHolder::get_Certificate metodu"
linktitle: "get_Certificate"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DigitalSignatures::CertificateHolder::get_Certificate metodu. C++'ta özel, genel anahtarları ve sertifika zincirini tutan X509Certificate2 örneğini döndürür."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.digitalsignatures/certificateholder/get_certificate/
---
## CertificateHolder::get_Certificate method


Özel ve genel anahtarları ve sertifika zincirini tutan **X509Certificate2** örneğini döndürür.

```cpp
System::SharedPtr<System::Security::Cryptography::X509Certificates::X509Certificate2> Aspose::Words::DigitalSignatures::CertificateHolder::get_Certificate()
```


### ReturnValue

**X509Certificate2****X509Certificate2** instance

## Örnekler



Bir belgede bulunan her imzanın doğrulanması ve bilgilerinin gösterilmesi nasıl yapılır gösterir.
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

## Ayrıca Bakınız

* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
