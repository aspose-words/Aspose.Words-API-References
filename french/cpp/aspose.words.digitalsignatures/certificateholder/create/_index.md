---
title: "Aspose::Words::DigitalSignatures::CertificateHolder::Create méthode"
linktitle: "Create"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DigitalSignatures::CertificateHolder::Create méthode. Crée un objet CertificateHolder à l'aide d'un tableau d'octets du magasin PKCS12 et de son mot de passe en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.digitalsignatures/certificateholder/create/
---
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) method


Crée l'objet [CertificateHolder](../) à l'aide d'un tableau d'octets du magasin PKCS12 et de son mot de passe.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::SharedPtr<System::Security::SecureString> &password)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | Un tableau d'octets contenant les données d'un certificat X.509. |
| password | const System::SharedPtr\<System::Security::SecureString\>\& | Le mot de passe requis pour accéder aux données du certificat X.509. |

### ReturnValue

Une instance de [CertificateHolder](../)

## Voir aussi

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) method


Crée l'objet [CertificateHolder](../) à l'aide d'un tableau d'octets du magasin PKCS12 et de son mot de passe.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::String &password)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | Un tableau d'octets contenant les données d'un certificat X.509. |
| password | const System::String\& | Le mot de passe requis pour accéder aux données du certificat X.509. |

### ReturnValue

Une instance de [CertificateHolder](../)

## Voir aussi

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&) method


Crée un objet [CertificateHolder](../) en utilisant le chemin du magasin PKCS12 et son mot de passe.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Le nom d'un fichier de certificat. |
| password | const System::String\& | Le mot de passe requis pour accéder aux données du certificat X.509. |

### ReturnValue

Une instance de [CertificateHolder](../)

## Exemples



Montre comment signer numériquement des documents.
```cpp
// Créez un certificat X.509 à partir d'un magasin PKCS#12, qui doit contenir une clé privée.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Créez un commentaire et une date qui seront appliqués avec notre nouvelle signature numérique.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Prenez un document non signé depuis le système de fichiers local via un flux de fichier,
// puis créez une copie signée déterminée par le nom de fichier du flux de sortie.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## Voir aussi

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&, const System::String\&) method


Crée un objet [CertificateHolder](../) en utilisant le chemin du magasin PKCS12, son mot de passe et l'alias permettant de trouver la clé privée et le certificat.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password, const System::String &alias)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Le nom d'un fichier de certificat. |
| password | const System::String\& | Le mot de passe requis pour accéder aux données du certificat X.509. |
| alias | const System::String\& | L'alias associé à un certificat et à sa clé privée |

### ReturnValue

Une instance de [CertificateHolder](../)

## Voir aussi

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
