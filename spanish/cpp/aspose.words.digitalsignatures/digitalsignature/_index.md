---
title: "Aspose::Words::DigitalSignatures::DigitalSignature clase"
linktitle: "DigitalSignature"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DigitalSignatures::DigitalSignature clase. Representa una firma digital en un documento y el resultado de su verificación. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class


Representa una firma digital en un documento y el resultado de su verificación. Para obtener más información, visite el artículo de documentación [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class DigitalSignature : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_ApplicationVersion](./get_applicationversion/)() | Obtiene la versión de la aplicación para la firma digital. |
| [get_CertificateHolder](./get_certificateholder/)() const | Devuelve el objeto titular del certificado que contiene el certificado utilizado para firmar el documento. |
| [get_ColorDepth](./get_colordepth/)() | Obtiene la profundidad de color para la firma digital. |
| [get_Comments](./get_comments/)() | Obtiene el comentario del propósito de la firma. |
| [get_HorizontalResolution](./get_horizontalresolution/)() | Obtiene la resolución horizontal para la firma digital. |
| [get_IssuerName](./get_issuername/)() | Devuelve el nombre distinguido del sujeto del emisor del certificado. |
| [get_IsValid](./get_isvalid/)() const | Devuelve **true** si esta firma digital es válida y el documento no ha sido manipulado. |
| [get_OfficeVersion](./get_officeversion/)() | Obtiene la versión de Office para la firma digital. |
| [get_SignatureType](./get_signaturetype/)() const | Obtiene el tipo de la firma digital. |
| [get_SignatureValue](./get_signaturevalue/)() const | Obtiene una matriz de bytes que representa el valor de la firma. |
| [get_SignTime](./get_signtime/)() const | Obtiene la hora en que se firmó el documento. |
| [get_SubjectName](./get_subjectname/)() | Devuelve el nombre distinguido del sujeto del certificado que se utilizó para firmar el documento. |
| [get_VerticalResolution](./get_verticalresolution/)() | Obtiene la resolución vertical para la firma digital. |
| [get_WindowsVersion](./get_windowsversion/)() | Obtiene la versión de Windows para la firma digital. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Devuelve una cadena fácil de usar que muestra el valor de este objeto. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
