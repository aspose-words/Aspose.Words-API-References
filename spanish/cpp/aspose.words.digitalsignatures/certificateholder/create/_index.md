---
title: "Aspose::Words::DigitalSignatures::CertificateHolder::Create método"
linktitle: "Create"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DigitalSignatures::CertificateHolder::Create método. Crea un objeto CertificateHolder usando el arreglo de bytes del almacén PKCS12 y su contraseña en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.digitalsignatures/certificateholder/create/
---
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) method


Crea un objeto [CertificateHolder](../) usando el arreglo de bytes del almacén PKCS12 y su contraseña.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::SharedPtr<System::Security::SecureString> &password)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | Una matriz de bytes que contiene datos de un certificado X.509. |
| password | const System::SharedPtr\<System::Security::SecureString\>\& | La contraseña requerida para acceder a los datos del certificado X.509. |

### ReturnValue

Una instancia de [CertificateHolder](../)

## Ver también

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) method


Crea un objeto [CertificateHolder](../) usando el arreglo de bytes del almacén PKCS12 y su contraseña.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::String &password)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | Una matriz de bytes que contiene datos de un certificado X.509. |
| password | const System::String\& | La contraseña requerida para acceder a los datos del certificado X.509. |

### ReturnValue

Una instancia de [CertificateHolder](../)

## Ver también

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&) method


Crea un objeto [CertificateHolder](../) usando la ruta al almacén PKCS12 y su contraseña.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | El nombre de un archivo de certificado. |
| password | const System::String\& | La contraseña requerida para acceder a los datos del certificado X.509. |

### ReturnValue

Una instancia de [CertificateHolder](../)

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

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&, const System::String\&) method


Crea un objeto [CertificateHolder](../) usando la ruta al almacén PKCS12, su contraseña y el alias mediante el cual se encontrará la clave privada y el certificado.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password, const System::String &alias)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | El nombre de un archivo de certificado. |
| password | const System::String\& | La contraseña requerida para acceder a los datos del certificado X.509. |
| alias | const System::String\& | El alias asociado para un certificado y su clave privada. |

### ReturnValue

Una instancia de [CertificateHolder](../)

## Ver también

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
