---
title: "Aspose::Words::LowCode::Splitter::ExtractPages‑Methode"
linktitle: "ExtractPages"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::Splitter::ExtractPages‑Methode. Extrahiert einen angegebenen Seitenbereich aus einem Dokumentstream und speichert die extrahierten Seiten in einen Ausgabestream unter Verwendung des angegebenen Speicherformats in C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.lowcode/splitter/extractpages/
---
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


Extrahiert einen angegebenen Seitenbereich aus einem Dokumenten-Stream und speichert die extrahierten Seiten in einem Ausgabestream unter Verwendung des angegebenen Speicherformats.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
| startPageIndex | int32_t | Der nullbasierte Index der ersten zu extrahierenden Seite. |
| pageCount | int32_t | Anzahl der zu extrahierenden Seiten. |

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) method


Extrahiert einen angegebenen Seitenbereich aus einem Dokumenten-Stream und speichert die extrahierten Seiten in einem Ausgabestream unter Verwendung des angegebenen Speicherformats.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, int32_t startPageIndex, int32_t pageCount)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
| startPageIndex | int32_t | Der nullbasierte Index der ersten zu extrahierenden Seite. |
| pageCount | int32_t | Anzahl der zu extrahierenden Seiten. |

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


Extrahiert einen angegebenen Seitenbereich aus einer Dokumentdatei und speichert die extrahierten Seiten in einer neuen Datei unter Verwendung des angegebenen Speicherformats.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |
| startPageIndex | int32_t | Der nullbasierte Index der ersten zu extrahierenden Seite. |
| pageCount | int32_t | Anzahl der zu extrahierenden Seiten. |

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) method


Extrahiert einen angegebenen Seitenbereich aus einer Dokumentdatei und speichert die extrahierten Seiten in einer neuen Datei unter Verwendung des angegebenen Speicherformats.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, int32_t startPageIndex, int32_t pageCount)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |
| startPageIndex | int32_t | Der nullbasierte Index der ersten zu extrahierenden Seite. |
| pageCount | int32_t | Anzahl der zu extrahierenden Seiten. |

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, int32_t, int32_t) method


Extrahiert einen angegebenen Seitenbereich aus einer Dokumentdatei und speichert die extrahierten Seiten in einer neuen Datei. Das Ausgabeformat wird durch die Erweiterung des Ausgabedateinamens bestimmt.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, int32_t startPageIndex, int32_t pageCount)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| startPageIndex | int32_t | Der nullbasierte Index der ersten zu extrahierenden Seite. |
| pageCount | int32_t | Anzahl der zu extrahierenden Seiten. |

## Siehe auch

* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
