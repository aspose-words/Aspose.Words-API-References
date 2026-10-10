---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures Methode"
linktitle: "RemoveAllSignatures"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures Methode. Entfernt alle digitalen Signaturen aus dem Dokument im Quell-Stream und schreibt das unsignierte Dokument in den Ziel-Stream. Die Ausgabe wird am Anfang des Streams geschrieben und die Streamgröße wird mit der Inhaltslänge aktualisiert. Die folgenden Formate sind für die Entfernung digitaler Signaturen kompatibel: Doc, Dot, Docx, Dotx, Docm, Dotm, Odt, Ott in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## DigitalSignatureUtil::RemoveAllSignatures(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Entfernt alle digitalen Signaturen aus dem Dokument im Quell-Stream und schreibt das unsignierte Dokument in den Ziel-Stream. **Die Ausgabe wird am Anfang des Streams geschrieben und die Streamgröße wird mit der Inhaltslänge aktualisiert.** Die folgenden Formate sind für die Entfernung digitaler Signaturen kompatibel: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(const System::SharedPtr<System::IO::Stream> &srcStream, const System::SharedPtr<System::IO::Stream> &dstStream)
```


## Beispiele



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

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::RemoveAllSignatures(const System::String\&, const System::String\&) method


Entfernt alle digitalen Signaturen aus der Quelldatei und schreibt die unsignierte Datei in die Zieldatei. Die folgenden Formate sind für die Entfernung digitaler Signaturen kompatibel: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(const System::String &srcFileName, const System::String &dstFileName)
```


## Beispiele



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

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::RemoveAllSignatures(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(std::basic_istream<CharType, Traits> &srcStream, std::basic_ostream<CharType, Traits> &dstStream)
```

## Siehe auch

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
