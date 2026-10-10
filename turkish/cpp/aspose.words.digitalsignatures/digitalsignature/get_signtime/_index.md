---
title: "Aspose::Words::DigitalSignatures::DigitalSignature::get_SignTime metodu"
linktitle: "get_SignTime"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DigitalSignatures::DigitalSignature::get_SignTime metodu. Belgenin imzalandığı zamanı C++'da alır."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.digitalsignatures/digitalsignature/get_signtime/
---
## DigitalSignature::get_SignTime method


Belgenin imzalanma zamanını alır.

```cpp
System::DateTime Aspose::Words::DigitalSignatures::DigitalSignature::get_SignTime() const
```


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

* Class [DigitalSignature](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
