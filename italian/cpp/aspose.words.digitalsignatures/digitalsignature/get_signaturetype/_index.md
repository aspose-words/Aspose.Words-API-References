---
title: "Aspose::Words::DigitalSignatures::DigitalSignature::get_SignatureType metodo"
linktitle: "get_SignatureType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DigitalSignatures::DigitalSignature::get_SignatureType. Ottiene il tipo della firma digitale in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.digitalsignatures/digitalsignature/get_signaturetype/
---
## DigitalSignature::get_SignatureType method


Ottiene il tipo della firma digitale.

```cpp
Aspose::Words::DigitalSignatures::DigitalSignatureType Aspose::Words::DigitalSignatures::DigitalSignature::get_SignatureType() const
```


## Esempi



Mostra come convalidare e visualizzare le informazioni su ogni firma in un documento.
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

## Vedi anche

* Enum [DigitalSignatureType](../../digitalsignaturetype/)
* Class [DigitalSignature](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
