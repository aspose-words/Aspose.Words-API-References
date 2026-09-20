---
title: "Método get_Comments de Aspose::Words::DigitalSignatures::DigitalSignature"
linktitle: "get_Comments"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método get_Comments de Aspose::Words::DigitalSignatures::DigitalSignature. Obtiene el comentario del propósito de la firma en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.digitalsignatures/digitalsignature/get_comments/
---
## DigitalSignature::get_Comments method


Obtiene el comentario del propósito de la firma.

```cpp
System::String Aspose::Words::DigitalSignatures::DigitalSignature::get_Comments()
```


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

* Class [DigitalSignature](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
