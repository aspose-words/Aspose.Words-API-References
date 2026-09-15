---
title: "Aspose::Words::DigitalSignatures::DigitalSignature::get_IsValid طريقة"
linktitle: "get_IsValid"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DigitalSignatures::DigitalSignature::get_IsValid طريقة. يرجع true إذا كانت هذه التوقيع الرقمي صالحًا ولم يتم العبث بالمستند في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.digitalsignatures/digitalsignature/get_isvalid/
---
## DigitalSignature::get_IsValid method


يعيد **true** إذا كان هذا التوقيع الرقمي صالحًا ولم يتم العبث بالمستند.

```cpp
bool Aspose::Words::DigitalSignatures::DigitalSignature::get_IsValid() const
```


## أمثلة



يوضح كيفية التحقق من صحة وعرض معلومات كل توقيع في المستند.
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

## انظر أيضًا

* Class [DigitalSignature](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
