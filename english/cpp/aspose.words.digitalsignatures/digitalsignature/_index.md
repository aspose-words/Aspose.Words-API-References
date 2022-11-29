---
title: DigitalSignature
second_title: Aspose.Words for C++ API Reference
description: Represents a digital signature on a document and the result of its verification.
type: docs
weight: 14
url: /cpp/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class


Represents a digital signature on a document and the result of its verification.

```cpp
class DigitalSignature : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | Returns the certificate holder object that contains the certificate was used to sign the document. |
| [get_Comments](./get_comments/)() const | Gets the signing purpose comment. |
| [get_IssuerName](./get_issuername/)() | Returns the subject distinguished name of the certificate isuuer. |
| [get_IsValid](./get_isvalid/)() const | Returns true if this digital signature is valid and the document has not been tampered with. |
| [get_SignatureType](./get_signaturetype/)() const | Gets the type of the digital signature. |
| [get_SignTime](./get_signtime/)() const | Gets the time the document was signed. |
| [get_SubjectName](./get_subjectname/)() | Returns the subject distinguished name of the certificate that was used to sign the document. |
| [ToString](./tostring/)() const override | Returns a user-friendly string that displays the value of this object. |

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

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words](../../)
