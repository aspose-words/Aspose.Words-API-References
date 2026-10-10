---
title: "Aspose::Words::DigitalSignatures::CertificateHolder::get_Certificate metodo"
linktitle: "get_Certificate"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DigitalSignatures::CertificateHolder::get_Certificate metodo. Restituisce l'istanza di X509Certificate2 che contiene le chiavi private, pubbliche e la catena di certificati in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.digitalsignatures/certificateholder/get_certificate/
---
## CertificateHolder::get_Certificate method


Restituisce l'istanza di **X509Certificate2** che contiene chiavi private, pubbliche e la catena di certificati.

```cpp
System::SharedPtr<System::Security::Cryptography::X509Certificates::X509Certificate2> Aspose::Words::DigitalSignatures::CertificateHolder::get_Certificate()
```


### ReturnValue

**X509Certificate2****X509Certificate2** instance

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

* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
