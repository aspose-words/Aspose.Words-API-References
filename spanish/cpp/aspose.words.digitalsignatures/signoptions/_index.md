---
title: "Clase Aspose::Words::DigitalSignatures::SignOptions"
linktitle: "SignOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::DigitalSignatures::SignOptions. Permite especificar opciones para la firma de documentos. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class


Permite especificar opciones para la firma de documentos. Para obtener más información, visite el artículo de documentación [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class SignOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_ApplicationVersion](./get_applicationversion/)() const | Obtiene o establece la versión de la aplicación para la firma digital. El valor predeterminado es "12.0". |
| [get_ColorDepth](./get_colordepth/)() const | Obtiene o establece la profundidad de color para la firma digital. El valor predeterminado es 32. |
| [get_Comments](./get_comments/)() const | Especifica los comentarios de la firma digital. El valor predeterminado es **empty string**. |
| [get_DecryptionPassword](./get_decryptionpassword/)() const | La contraseña para descifrar el documento fuente. El valor predeterminado es **empty string**. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | Obtiene o establece la resolución horizontal para la firma digital. El valor predeterminado es 1920. |
| [get_OfficeVersion](./get_officeversion/)() const | Obtiene o establece la versión de Office para la firma digital. El valor predeterminado es "12.0". |
| [get_ProviderId](./get_providerid/)() const | Especifica el ID de clase del proveedor de firma. El valor predeterminado es **Empty (all zeroes) Guid**. |
| [get_SignatureLineId](./get_signaturelineid/)() const | Identificador de la línea de firma. El valor predeterminado es **Empty (all zeroes) Guid**. |
| [get_SignatureLineImage](./get_signaturelineimage/)() const | La imagen que se mostrará en el [SignatureLine](../../aspose.words.drawing/signatureline/) asociado. El valor predeterminado es **null**. |
| [get_SignTime](./get_signtime/)() const | La fecha de la firma. El valor predeterminado es **current time** (**Now**). |
| [get_VerticalResolution](./get_verticalresolution/)() const | Obtiene o establece la resolución vertical para la firma digital. El valor predeterminado es 1200. |
| [get_WindowsVersion](./get_windowsversion/)() const | Obtiene o establece la versión de Windows para la firma digital. El valor predeterminado es "6.1". |
| [get_XmlDsigLevel](./get_xmldsiglevel/)() const | Especifica el nivel de una firma digital basado en el estándar XML-DSig. El valor predeterminado es [XmlDSig](../xmldsiglevel/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ApplicationVersion](./set_applicationversion/)(const System::String\&) | Método set para [Aspose::Words::DigitalSignatures::SignOptions::get_ApplicationVersion](./get_applicationversion/). |
| [set_ColorDepth](./set_colordepth/)(int32_t) | Método set para [Aspose::Words::DigitalSignatures::SignOptions::get_ColorDepth](./get_colordepth/). |
| [set_Comments](./set_comments/)(const System::String\&) | Método set para [Aspose::Words::DigitalSignatures::SignOptions::get_Comments](./get_comments/). |
| [set_DecryptionPassword](./set_decryptionpassword/)(const System::String\&) | Método set para [Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword](./get_decryptionpassword/). |
| [set_HorizontalResolution](./set_horizontalresolution/)(int32_t) | Método set para [Aspose::Words::DigitalSignatures::SignOptions::get_HorizontalResolution](./get_horizontalresolution/). |
| [set_OfficeVersion](./set_officeversion/)(const System::String\&) | Método set para [Aspose::Words::DigitalSignatures::SignOptions::get_OfficeVersion](./get_officeversion/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | Método set para [Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId](./get_providerid/). |
| [set_SignatureLineId](./set_signaturelineid/)(System::Guid) | Identificador de la línea de firma. El valor predeterminado es **Empty (all zeroes) Guid**. |
| [set_SignatureLineImage](./set_signaturelineimage/)(const System::ArrayPtr\<uint8_t\>\&) | La imagen que se mostrará en el [SignatureLine](../../aspose.words.drawing/signatureline/) asociado. El valor predeterminado es **null**. |
| [set_SignTime](./set_signtime/)(System::DateTime) | Método set para [Aspose::Words::DigitalSignatures::SignOptions::get_SignTime](./get_signtime/). |
| [set_VerticalResolution](./set_verticalresolution/)(int32_t) | Método set para [Aspose::Words::DigitalSignatures::SignOptions::get_VerticalResolution](./get_verticalresolution/). |
| [set_WindowsVersion](./set_windowsversion/)(const System::String\&) | Método set para [Aspose::Words::DigitalSignatures::SignOptions::get_WindowsVersion](./get_windowsversion/). |
| [set_XmlDsigLevel](./set_xmldsiglevel/)(Aspose::Words::DigitalSignatures::XmlDsigLevel) | Método set para [Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel](./get_xmldsiglevel/). |
| [SignOptions](./signoptions/)() |  |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo firmar digitalmente documentos.
```cpp
// Crea un certificado X.509 a partir de un almacén PKCS#12, que debe contener una clave privada.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Crea un comentario y una fecha que se aplicarán con nuestra nueva firma digital.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Obtén un documento sin firmar del sistema de archivos local mediante un flujo de archivo,
// luego crea una copia firmada del mismo determinada por el nombre de archivo del flujo de salida.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## Ver también

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
