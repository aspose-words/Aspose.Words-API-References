---
title: "Aspose::Words::DigitalSignatures::CertificateHolder clase"
linktitle: "CertificateHolder"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DigitalSignatures::CertificateHolder clase. Representa un contenedor de una instancia X509Certificate2. Para obtener más información, visita el artículo de documentación en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class


Representa un contenedor de la instancia **X509Certificate2**. Para obtener más información, visite el artículo de documentación [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class CertificateHolder : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) | Crea un objeto [CertificateHolder](./) usando el arreglo de bytes del almacén PKCS12 y su contraseña. |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) | Crea un objeto [CertificateHolder](./) usando el arreglo de bytes del almacén PKCS12 y su contraseña. |
| static [Create](./create/)(const System::String\&, const System::String\&) | Crea un objeto [CertificateHolder](./) usando la ruta al almacén PKCS12 y su contraseña. |
| static [Create](./create/)(const System::String\&, const System::String\&, const System::String\&) | Crea un objeto [CertificateHolder](./) usando la ruta al almacén PKCS12, su contraseña y el alias mediante el cual se encontrará la clave privada y el certificado. |
| [get_Certificate](./get_certificate/)() | Devuelve la instancia de **X509Certificate2** que contiene claves privadas, públicas y la cadena de certificados. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Observaciones


[CertificateHolder](./) can be created by static factory methods only. It contains an instance of **X509Certificate2** which is used to introduce private, public keys and certificate chains into the system. This class is applied in [DigitalSignatureUtil](../digitalsignatureutil/) and [PdfDigitalSignatureDetails](../../aspose.words.saving/pdfdigitalsignaturedetails/) instead of obsolete methods with **X509Certificate2** as parameters.

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


Muestra cómo firmar un archivo de documento cifrado.
```cpp
// Crea un certificado X.509 a partir de un almacén PKCS#12, que debe contener una clave privada.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Crea un comentario, una fecha y una contraseña de descifrado que se aplicarán con nuestra nueva firma digital.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

// Establezca un nombre de archivo del sistema local para el documento de entrada sin firmar, y un nombre de archivo de salida para su nueva copia firmada digitalmente.
System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.DecryptionPassword.docx";

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## Ver también

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
