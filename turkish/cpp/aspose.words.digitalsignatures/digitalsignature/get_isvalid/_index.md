---
title: "Aspose::Words::DigitalSignatures::DigitalSignature::get_IsValid metodu"
linktitle: "get_IsValid"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DigitalSignatures::DigitalSignature::get_IsValid metodu. Bu dijital imza geçerli ise ve belge C++'da değiştirilmemişse true döndürür."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.digitalsignatures/digitalsignature/get_isvalid/
---
## DigitalSignature::get_IsValid method


Bu dijital imza geçerli ve belge değiştirilmemişse **true** döndürür.

```cpp
bool Aspose::Words::DigitalSignatures::DigitalSignature::get_IsValid() const
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
