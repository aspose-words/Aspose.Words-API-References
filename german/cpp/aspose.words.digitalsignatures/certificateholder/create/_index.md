---
title: "Aspose::Words::DigitalSignatures::CertificateHolder::Create Methode"
linktitle: "Create"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DigitalSignatures::CertificateHolder::Create Methode. Erstellt ein CertificateHolder-Objekt mithilfe eines Byte-Arrays des PKCS12-Speichers und dessen Passwort in C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.digitalsignatures/certificateholder/create/
---
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) method


Erstellt ein [CertificateHolder](../)-Objekt mithilfe eines Byte-Arrays des PKCS12-Speichers und dessen Passwort.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::SharedPtr<System::Security::SecureString> &password)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | Ein Byte-Array, das Daten aus einem X.509-Zertifikat enthält. |
| password | const System::SharedPtr\<System::Security::SecureString\>\& | Das Passwort, das zum Zugriff auf die X.509-Zertifikatsdaten erforderlich ist. |

### ReturnValue

Eine Instanz von [CertificateHolder](../)

## Siehe auch

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) method


Erstellt ein [CertificateHolder](../)-Objekt mithilfe eines Byte-Arrays des PKCS12-Speichers und dessen Passwort.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::String &password)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | Ein Byte-Array, das Daten aus einem X.509-Zertifikat enthält. |
| password | const System::String\& | Das Passwort, das zum Zugriff auf die X.509-Zertifikatsdaten erforderlich ist. |

### ReturnValue

Eine Instanz von [CertificateHolder](../)

## Siehe auch

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&) method


Erstellt ein [CertificateHolder](../)-Objekt mithilfe des Pfads zum PKCS12-Speicher und dessen Passwort.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Der Name einer Zertifikatsdatei. |
| password | const System::String\& | Das Passwort, das zum Zugriff auf die X.509-Zertifikatsdaten erforderlich ist. |

### ReturnValue

Eine Instanz von [CertificateHolder](../)

## Beispiele



Zeigt, wie man Dokumente digital signiert.
```cpp
// Erstellen Sie ein X.509-Zertifikat aus einem PKCS#12-Store, der einen privaten Schlüssel enthalten sollte.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Erstellen Sie einen Kommentar und ein Datum, die mit unserer neuen digitalen Signatur angewendet werden.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Nehmen Sie ein unsigniertes Dokument aus dem lokalen Dateisystem über einen Dateistream,
// und erstellen Sie dann eine signierte Kopie davon, bestimmt durch den Dateinamen des Ausgabedateistreams.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## Siehe auch

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&, const System::String\&) method


Erstellt ein [CertificateHolder](../)-Objekt mithilfe des Pfads zum PKCS12-Speicher, dessen Passwort und dem Alias, über den der private Schlüssel und das Zertifikat gefunden werden.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password, const System::String &alias)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Der Name einer Zertifikatsdatei. |
| password | const System::String\& | Das Passwort, das zum Zugriff auf die X.509-Zertifikatsdaten erforderlich ist. |
| alias | const System::String\& | Der zugehörige Alias für ein Zertifikat und dessen privaten Schlüssel |

### ReturnValue

Eine Instanz von [CertificateHolder](../)

## Siehe auch

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
