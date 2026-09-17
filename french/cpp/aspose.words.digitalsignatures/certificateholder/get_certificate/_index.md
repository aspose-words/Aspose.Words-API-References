---
title: "Aspose::Words::DigitalSignatures::CertificateHolder::get_Certificate méthode"
linktitle: "get_Certificate"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DigitalSignatures::CertificateHolder::get_Certificate méthode. Retourne l'instance de X509Certificate2 qui contient les clés privées, publiques et la chaîne de certificats en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.digitalsignatures/certificateholder/get_certificate/
---
## CertificateHolder::get_Certificate method


Renvoie l'instance de **X509Certificate2** qui contient les clés privées, publiques et la chaîne de certificats.

```cpp
System::SharedPtr<System::Security::Cryptography::X509Certificates::X509Certificate2> Aspose::Words::DigitalSignatures::CertificateHolder::get_Certificate()
```


### ReturnValue

**X509Certificate2****X509Certificate2** instance

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

* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
