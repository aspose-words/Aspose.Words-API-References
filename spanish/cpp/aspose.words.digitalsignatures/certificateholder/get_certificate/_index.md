---
title: "Aspose::Words::DigitalSignatures::CertificateHolder::get_Certificate método"
linktitle: "get_Certificate"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DigitalSignatures::CertificateHolder::get_Certificate método. Devuelve la instancia de X509Certificate2 que contiene claves privadas, públicas y la cadena de certificados en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.digitalsignatures/certificateholder/get_certificate/
---
## CertificateHolder::get_Certificate method


Devuelve la instancia de **X509Certificate2** que contiene claves privadas, públicas y la cadena de certificados.

```cpp
System::SharedPtr<System::Security::Cryptography::X509Certificates::X509Certificate2> Aspose::Words::DigitalSignatures::CertificateHolder::get_Certificate()
```


### ReturnValue

**X509Certificate2****X509Certificate2** instance

## Ejemplos



Muestra cómo validar y mostrar información sobre cada firma en un documento.
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

## Ver también

* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
