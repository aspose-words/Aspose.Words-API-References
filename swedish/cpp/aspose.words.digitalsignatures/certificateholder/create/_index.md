---
title: "Aspose::Words::DigitalSignatures::CertificateHolder::Create‑metod"
linktitle: "Create"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DigitalSignatures::CertificateHolder::Create‑metod. Skapar ett CertificateHolder‑objekt med hjälp av en bytearray från PKCS12‑lagret och dess lösenord i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.digitalsignatures/certificateholder/create/
---
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) method


Skapar [CertificateHolder](../)‑objekt med hjälp av en bytearray från PKCS12‑lagret och dess lösenord.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::SharedPtr<System::Security::SecureString> &password)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | En bytearray som innehåller data från ett X.509‑certifikat. |
| password | const System::SharedPtr\<System::Security::SecureString\>\& | Lösenordet som krävs för att komma åt X.509‑certifikatdata. |

### ReturnValue

En instans av [CertificateHolder](../)

## Se även

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) method


Skapar [CertificateHolder](../)‑objekt med hjälp av en bytearray från PKCS12‑lagret och dess lösenord.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::String &password)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | En bytearray som innehåller data från ett X.509‑certifikat. |
| password | const System::String\& | Lösenordet som krävs för att komma åt X.509‑certifikatdata. |

### ReturnValue

En instans av [CertificateHolder](../)

## Se även

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&) method


Skapar [CertificateHolder](../)-objekt med sökväg till PKCS12-lagring och dess lösenord.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | const System::String\& | Namnet på en certifikatfil. |
| password | const System::String\& | Lösenordet som krävs för att komma åt X.509‑certifikatdata. |

### ReturnValue

En instans av [CertificateHolder](../)

## Exempel



Visar hur man digitalt signerar dokument.
```cpp
// Skapa ett X.509‑certifikat från en PKCS#12‑butik, som bör innehålla en privat nyckel.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Skapa en kommentar och ett datum som kommer att tillämpas med vår nya digitala signatur.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Hämta ett osignerat dokument från det lokala filsystemet via en filström,
// sedan skapa en signerad kopia av den bestämd av filnamnet på utdatafilströmmen.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## Se även

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&, const System::String\&) method


Skapar [CertificateHolder](../)-objekt med sökväg till PKCS12-lagring, dess lösenord och aliaset som används för att hitta den privata nyckeln och certifikatet.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password, const System::String &alias)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | const System::String\& | Namnet på en certifikatfil. |
| password | const System::String\& | Lösenordet som krävs för att komma åt X.509‑certifikatdata. |
| alias | const System::String\& | Det associerade aliaset för ett certifikat och dess privata nyckel |

### ReturnValue

En instans av [CertificateHolder](../)

## Se även

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
