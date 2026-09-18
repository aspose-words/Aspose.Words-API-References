---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil class"
linktitle: "DigitalSignatureUtil"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil class. Bietet Methoden zum Signieren von Dokumenten. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class


Stellt Methoden zum Signieren von Dokumenten bereit. Weitere Informationen finden Sie im [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) Dokumentationsartikel.

```cpp
class DigitalSignatureUtil
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [DigitalSignatureUtil](./digitalsignatureutil/)() |  |
| static [LoadSignatures](./loadsignatures/)(const System::String\&) | Lädt digitale Signaturen aus dem Dokument. |
| static [LoadSignatures](./loadsignatures/)(const System::SharedPtr\<System::IO::Stream\>\&) | Lädt digitale Signaturen aus dem Dokument mithilfe eines Streams. |
| static [LoadSignatures](./loadsignatures/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [RemoveAllSignatures](./removeallsignatures/)(const System::String\&, const System::String\&) | Entfernt alle digitalen Signaturen aus der Quelldatei und schreibt die unsignierte Datei in die Zieldatei. Die folgenden Formate sind für das Entfernen digitaler Signaturen kompatibel: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [RemoveAllSignatures](./removeallsignatures/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Entfernt alle digitalen Signaturen aus dem Dokument im Quellstream und schreibt das unsignierte Dokument in den Zielstream. **Die Ausgabe wird am Anfang des Streams geschrieben und die Streamgröße wird mit der Inhaltslänge aktualisiert.** Die folgenden Formate sind für das Entfernen digitaler Signaturen kompatibel: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [RemoveAllSignatures](./removeallsignatures/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Sign](./sign/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Signiert das Quelldokument mit dem angegebenen [CertificateHolder](../certificateholder/) und [SignOptions](../signoptions/) mittels digitaler Signatur und schreibt das signierte Dokument in den Zielstream. Unterstützte Formate sind: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). **Die Ausgabe wird am Anfang des Streams geschrieben und die Streamgröße wird mit der Inhaltslänge aktualisiert.** |
| static [Sign](./sign/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Signiert das Quelldokument mit dem angegebenen [CertificateHolder](../certificateholder/) und [SignOptions](../signoptions/) mittels digitaler Signatur und schreibt das signierte Dokument in die Zieldatei. Unterstützte Formate sind: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [Sign](./sign/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Signiert das Quell‑Dokument mit dem angegebenen [CertificateHolder](../certificateholder/) mittels digitaler Signatur und schreibt das signierte Dokument in den Ziel‑Stream. Unterstützte Formate sind: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/).**Die Ausgabe wird am Anfang des Streams geschrieben und die Streamgröße wird mit der Inhaltslänge aktualisiert.** |
| static [Sign](./sign/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Signiert das Quell‑Dokument mit dem angegebenen [CertificateHolder](../certificateholder/) mittels digitaler Signatur und schreibt das signierte Dokument in die Zieldatei. Unterstützte Formate sind: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [Sign](./sign/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>, System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>) |  |
| static [Sign](./sign/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>) |  |
## Hinweise


Da die digitale Signatur mit dem Dateiinhalt und nicht mit dem [Document](../../aspose.words/document/) Objektmodell arbeitet, werden diese Methoden in eine separate Klasse ausgelagert.

Unterstützte Formate sind: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/).

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

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
