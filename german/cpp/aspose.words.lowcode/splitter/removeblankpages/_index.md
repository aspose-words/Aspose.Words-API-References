---
title: "Aspose::Words::LowCode::Splitter::RemoveBlankPages‑Methode"
linktitle: "RemoveBlankPages"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::Splitter::RemoveBlankPages‑Methode. Entfernt leere Seiten aus einem in einem Eingabestream bereitgestellten Dokument und speichert das aktualisierte Dokument in einen Ausgabestream im angegebenen Speicherformat. Gibt eine Liste von Seitenzahlen zurück, die in C++ entfernt wurden."
type: docs
weight: 2000
url: /de/cpp/aspose.words.lowcode/splitter/removeblankpages/
---
## Splitter::RemoveBlankPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Entfernt leere Seiten aus einem Dokument, das in einem Eingabestream bereitgestellt wird, und speichert das aktualisierte Dokument in einem Ausgabestream im angegebenen Speicherformat. Gibt eine Liste der Seitenzahlen zurück, die entfernt wurden.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |

### ReturnValue

Liste von Seitenzahlen wurde als leer betrachtet und entfernt.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Entfernt leere Seiten aus einem Dokument, das in einem Eingabestream bereitgestellt wird, und speichert das aktualisierte Dokument in einem Ausgabestream im angegebenen Speicherformat. Gibt eine Liste der Seitenzahlen zurück, die entfernt wurden.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Eingabestream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Ausgabestream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |

### ReturnValue

Liste von Seitenzahlen wurde als leer betrachtet und entfernt.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&) method


Entfernt leere Seiten aus dem Dokument und speichert die Ausgabe. Gibt eine Liste der Seitenzahlen zurück, die entfernt wurden.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |

### ReturnValue

Liste von Seitenzahlen wurde als leer betrachtet und entfernt.

## Siehe auch

* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Entfernt leere Seiten aus dem Dokument und speichert die Ausgabe im angegebenen Format. Gibt eine Liste der Seitenzahlen zurück, die entfernt wurden.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat. |

### ReturnValue

Liste von Seitenzahlen wurde als leer betrachtet und entfernt.

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Entfernt leere Seiten aus dem Dokument und speichert die Ausgabe im angegebenen Format. Gibt eine Liste der Seitenzahlen zurück, die entfernt wurden.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | const System::String\& | Der Eingabedateiname. |
| outputFileName | const System::String\& | Der Name der Ausgabedatei. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Die Speicheroptionen. |

### ReturnValue

Liste von Seitenzahlen wurde als leer betrachtet und entfernt.

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
