---
title: Aspose::Words::DigitalSignatures::DigitalSignature::get_SignTime method
linktitle: get_SignTime
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::DigitalSignature::get_SignTime method. Gets the time the document was signed in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.digitalsignatures/digitalsignature/get_signtime/
---
## DigitalSignature::get_SignTime method


Gets the time the document was signed.

```cpp
System::DateTime Aspose::Words::DigitalSignatures::DigitalSignature::get_SignTime() const
```


## Examples



Shows how to validate and display information about each signature in a document. 
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

## See Also

* Class [DigitalSignature](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
