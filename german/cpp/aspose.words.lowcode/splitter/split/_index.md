---
title: "Aspose::Words::LowCode::Splitter::Split‑Methode"
linktitle: "Split"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::Splitter::Split‑Methode. Teilt ein Dokument aus einem Eingabestream in mehrere Teile basierend auf den angegebenen Split‑Optionen und gibt die resultierenden Teile als Array von Streams im angegebenen Speicherformat in C++ zurück."
type: docs
weight: 3000
url: /de/cpp/aspose.words.lowcode/splitter/split/
---
## Splitter::Split(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Teilt ein Dokument aus einem Eingabestream anhand der angegebenen Aufteilungsoptionen in mehrere Teile und gibt die resultierenden Teile als Array von Streams im angegebenen Speicherformat zurück.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Splitter::Split(const System::SharedPtr<System::IO::Stream> &inputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) Split-Optionen. |

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Teilt ein Dokument aus einem Eingabestream anhand der angegebenen Aufteilungsoptionen in mehrere Teile und gibt die resultierenden Teile als Array von Streams im angegebenen Speicherformat zurück.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Splitter::Split(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) Split-Optionen. |

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Teilt ein Dokument anhand der angegebenen Aufteilungsoptionen in mehrere Teile und speichert die resultierenden Teile in Dateien im angegebenen Speicherformat.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Ausgabedateiname, der verwendet wird, um Dateinamen für Dokumentteile nach der Regel \"outputFile_partIndex.extension\" zu erzeugen. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) Split-Optionen. |

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Teilt ein Dokument anhand der angegebenen Aufteilungsoptionen in mehrere Teile und speichert die resultierenden Teile in Dateien. Das Ausgabe-Dateiformat wird durch die Erweiterung des Ausgabedateinamens bestimmt.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Ausgabedateiname, der verwendet wird, um Dateinamen für Dokumentteile nach der Regel \"outputFile_partIndex.extension\" zu erzeugen. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) Split-Optionen. |

## Siehe auch

* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Teilt ein Dokument anhand der angegebenen Aufteilungsoptionen in mehrere Teile und speichert die resultierenden Teile in Dateien im angegebenen Speicherformat.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Ausgabedateiname, der verwendet wird, um Dateinamen für Dokumentteile nach der Regel \"outputFile_partIndex.extension\" zu erzeugen. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) Split-Optionen. |

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
