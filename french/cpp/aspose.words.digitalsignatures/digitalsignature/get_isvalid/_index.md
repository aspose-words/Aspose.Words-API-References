---
title: "Aspose::Words::DigitalSignatures::DigitalSignature::get_IsValid méthode"
linktitle: "get_IsValid"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DigitalSignatures::DigitalSignature::get_IsValid méthode. Renvoie true si cette signature numérique est valide et que le document n'a pas été altéré en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.digitalsignatures/digitalsignature/get_isvalid/
---
## DigitalSignature::get_IsValid method


Renvoie **true** si cette signature numérique est valide et que le document n'a pas été altéré.

```cpp
bool Aspose::Words::DigitalSignatures::DigitalSignature::get_IsValid() const
```


## Exemples



Montre comment valider et afficher les informations sur chaque signature dans un document.
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

## Voir aussi

* Class [DigitalSignature](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
