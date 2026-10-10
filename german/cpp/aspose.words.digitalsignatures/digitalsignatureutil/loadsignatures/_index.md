---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures Methode"
linktitle: "LoadSignatures"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures Methode. Lädt digitale Signaturen aus dem Dokument über einen Stream in C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## DigitalSignatureUtil::LoadSignatures(const System::SharedPtr\<System::IO::Stream\>\&) method


Lädt digitale Signaturen aus dem Dokument mithilfe eines Streams.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Datenstrom | const System::SharedPtr\<System::IO::Stream\>\& | Stream mit dem Dokument. |

### ReturnValue

Sammlung digitaler Signaturen. Gibt eine leere Sammlung zurück, wenn die Datei nicht signiert ist.

## Beispiele



Zeigt, wie Signaturen aus einem digital signierten Dokument geladen werden.
```cpp
// Es gibt zwei Möglichkeiten, die Sammlung digitaler Signaturen eines signierten Dokuments mit der Klasse DigitalSignatureUtil zu laden.
// 1 -  Laden aus einem Dokument über einen Dateinamen im lokalen Dateisystem:
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_MyDir() + u"Digitally signed.docx");

// Wenn diese Sammlung nicht leer ist, können wir überprüfen, dass das Dokument digital signiert ist.
ASSERT_EQ(1, digitalSignatures->get_Count());

// 2 -  Laden aus einem Dokument über einen FileStream:
{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Digitally signed.docx", System::IO::FileMode::Open);
    digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(stream);
    ASSERT_EQ(1, digitalSignatures->get_Count());
}
```

## Siehe auch

* Class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::LoadSignatures(const System::String\&) method


Lädt digitale Signaturen aus dem Dokument.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(const System::String &fileName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Pfad zum Dokument. |

### ReturnValue

Sammlung digitaler Signaturen. Gibt eine leere Sammlung zurück, wenn die Datei nicht signiert ist.

## Beispiele



Zeigt, wie Signaturen aus einem digital signierten Dokument geladen werden.
```cpp
// Es gibt zwei Möglichkeiten, die Sammlung digitaler Signaturen eines signierten Dokuments mit der Klasse DigitalSignatureUtil zu laden.
// 1 -  Laden aus einem Dokument über einen Dateinamen im lokalen Dateisystem:
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_MyDir() + u"Digitally signed.docx");

// Wenn diese Sammlung nicht leer ist, können wir überprüfen, dass das Dokument digital signiert ist.
ASSERT_EQ(1, digitalSignatures->get_Count());

// 2 -  Laden aus einem Dokument über einen FileStream:
{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Digitally signed.docx", System::IO::FileMode::Open);
    digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(stream);
    ASSERT_EQ(1, digitalSignatures->get_Count());
}
```


Zeigt, wie digitale Signaturen aus einem digital signierten Dokument entfernt werden.
```cpp
// Es gibt zwei Möglichkeiten, die Klasse DigitalSignatureUtil zu verwenden, um digitale Signaturen zu entfernen
// aus einem signierten Dokument, indem eine unsignierte Kopie an einem anderen Ort im lokalen Dateisystem gespeichert wird.
// 1 - Bestimmen Sie die Speicherorte sowohl des signierten Dokuments als auch der unsignierten Kopie anhand von Dateinamen-Strings:
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(get_MyDir() + u"Digitally signed.docx", get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Bestimmen Sie die Speicherorte sowohl des signierten Dokuments als auch der unsignierten Kopie anhand von FileStreams:
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Digitally signed.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromStream.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(streamIn, streamOut);
    }
}

// Verifizieren Sie, dass beide Ausgabedokumente keine digitalen Signaturen enthalten.
ASSERT_EQ(0, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromString.docx")->get_Count());
ASSERT_EQ(0, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromStream.docx")->get_Count());
```

## Siehe auch

* Class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::LoadSignatures(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(std::basic_istream<CharType, Traits> &stream)
```

## Siehe auch

* Class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
