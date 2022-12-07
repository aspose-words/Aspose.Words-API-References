---
title: get_Comments
second_title: Aspose.Words for C++ API Reference
description: Gets the signing purpose comment.
type: docs
weight: 27
url: /cpp/aspose.words.digitalsignatures/digitalsignature/get_comments/
---
## DigitalSignature::get_Comments method


Gets the signing purpose comment.

```cpp
System::String Aspose::Words::DigitalSignatures::DigitalSignature::get_Comments() const
```


## Examples



Shows how to validate and display information about each signature in a document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Digitally signed.docx");

for (const auto& signature : doc->get_DigitalSignatures())
{
    std::cout << (signature->get_IsValid() ? String(u"Valid") : String(u"Invalid")) << " signature: " << std::endl;
    std::cout << "\tReason:\t" << signature->get_Comments() << std::endl;
    std::cout << String::Format(u"\tType:\t{0}", signature->get_SignatureType()) << std::endl;
    std::cout << "\tSign time:\t" << signature->get_SignTime() << std::endl;
    std::cout << "\tSubject name:\t" << signature->get_CertificateHolder()->get_Certificate()->get_SubjectName() << std::endl;
    std::cout << "\tIssuer name:\t" << signature->get_CertificateHolder()->get_Certificate()->get_IssuerName()->get_Name() << std::endl;
    std::cout << std::endl;
}
```

## See Also

* Class [DigitalSignature](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words](../../../)
