---
title: "Aspose::Words::DigitalSignatures::CertificateHolder::Create metodo"
linktitle: "Create"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DigitalSignatures::CertificateHolder::Create metodo. Crea un oggetto CertificateHolder usando l'array di byte del contenitore PKCS12 e la sua password in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.digitalsignatures/certificateholder/create/
---
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) method


Crea un oggetto [CertificateHolder](../) usando l'array di byte del contenitore PKCS12 e la sua password.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::SharedPtr<System::Security::SecureString> &password)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | Un array di byte che contiene dati da un certificato X.509. |
| password | const System::SharedPtr\<System::Security::SecureString\>\& | La password necessaria per accedere ai dati del certificato X.509. |

### ReturnValue

Un'istanza di [CertificateHolder](../)

## Vedi anche

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) method


Crea un oggetto [CertificateHolder](../) usando l'array di byte del contenitore PKCS12 e la sua password.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::String &password)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | Un array di byte che contiene dati da un certificato X.509. |
| password | const System::String\& | La password necessaria per accedere ai dati del certificato X.509. |

### ReturnValue

Un'istanza di [CertificateHolder](../)

## Vedi anche

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&) method


Crea l'oggetto [CertificateHolder](../) utilizzando il percorso del negozio PKCS12 e la sua password.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Il nome di un file di certificato. |
| password | const System::String\& | La password necessaria per accedere ai dati del certificato X.509. |

### ReturnValue

Un'istanza di [CertificateHolder](../)

## Esempi



Mostra come firmare digitalmente i documenti.
```cpp
// Crea un certificato X.509 da un archivio PKCS#12, che dovrebbe contenere una chiave privata.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Crea un commento e una data che saranno applicati con la nostra nuova firma digitale.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Prendi un documento non firmato dal file system locale tramite un flusso di file,
// quindi crea una copia firmata determinata dal nome file del flusso di file di output.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## Vedi anche

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&, const System::String\&) method


Crea l'oggetto [CertificateHolder](../) utilizzando il percorso del negozio PKCS12, la sua password e l'alias con cui verranno trovati la chiave privata e il certificato.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password, const System::String &alias)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Il nome di un file di certificato. |
| password | const System::String\& | La password necessaria per accedere ai dati del certificato X.509. |
| alias | const System::String\& | L'alias associato a un certificato e alla sua chiave privata |

### ReturnValue

Un'istanza di [CertificateHolder](../)

## Vedi anche

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
