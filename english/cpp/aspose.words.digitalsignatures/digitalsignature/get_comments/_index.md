---
title: Aspose::Words::DigitalSignatures::DigitalSignature::get_Comments method
linktitle: get_Comments
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::DigitalSignature::get_Comments method. Gets the signing purpose comment in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.digitalsignatures/digitalsignature/get_comments/
---
## DigitalSignature::get_Comments method


Gets the signing purpose comment.

```cpp
System::String Aspose::Words::DigitalSignatures::DigitalSignature::get_Comments()
```


## Examples



Shows how to validate and display information about each signature in a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Digitally signed.docx"));

for (auto&& signature : doc->get_DigitalSignatures())
{
    System::Console::WriteLine(System::String::Format(u"{0} signature: ", signature->get_IsValid() ? System::String(u"Valid") : System::String(u"Invalid")));
    System::Console::WriteLine(System::String::Format(u"\tReason:\t{0}", signature->get_Comments()));
    System::Console::WriteLine(System::String::Format(u"\tType:\t{0}", signature->get_SignatureType()));
    System::Console::WriteLine(System::String::Format(u"\tSign time:\t{0}", signature->get_SignTime()));
    System::Console::WriteLine(System::String::Format(u"\tSubject name:\t{0}", signature->get_CertificateHolder()->get_Certificate()->get_SubjectName()));
    System::Console::WriteLine(System::String::Format(u"\tIssuer name:\t{0}", signature->get_CertificateHolder()->get_Certificate()->get_IssuerName()->get_Name()));
    System::Console::WriteLine();
}
```

## See Also

* Class [DigitalSignature](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
