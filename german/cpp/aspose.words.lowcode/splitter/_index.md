---
title: "Aspose::Words::LowCode::Splitter Klasse"
linktitle: "Splitter"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::Splitter Klasse. Stellt Methoden bereit, die dazu dienen, Dokumente anhand verschiedener Kriterien in C++ in Teile zu splitten."
type: docs
weight: 1500
url: /de/cpp/aspose.words.lowcode/splitter/
---
## Splitter class


Stellt Methoden bereit, die dazu bestimmt sind, Dokumente anhand verschiedener Kriterien in Teile zu splitten.

```cpp
class Splitter : public Aspose::Words::LowCode::Processor
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::SplitterContext\>\&) | Erstellt eine neue Instanz des Splitter-Prozessors. |
| [Execute](../processor/execute/)() | Führt die Prozessoraktion aus. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Führt die Prozessoraktion aus und ermöglicht das Abbrechen des Dokumentverarbeitungsvorgangs mithilfe des angegebenen Abbruchtokens. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, int32_t, int32_t) | Extrahiert einen angegebenen Seitenbereich aus einer Dokumentdatei und speichert die extrahierten Seiten in einer neuen Datei. Das Ausgabeformat wird durch die Erweiterung des Ausgabedateinamens bestimmt. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) | Extrahiert einen angegebenen Seitenbereich aus einer Dokumentdatei und speichert die extrahierten Seiten in einer neuen Datei unter Verwendung des angegebenen Speicherformats. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | Extrahiert einen angegebenen Seitenbereich aus einer Dokumentdatei und speichert die extrahierten Seiten in einer neuen Datei unter Verwendung des angegebenen Speicherformats. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) | Extrahiert einen angegebenen Seitenbereich aus einem Dokumenten-Stream und speichert die extrahierten Seiten in einem Ausgabestream unter Verwendung des angegebenen Speicherformats. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | Extrahiert einen angegebenen Seitenbereich aus einem Dokumenten-Stream und speichert die extrahierten Seiten in einem Ausgabestream unter Verwendung des angegebenen Speicherformats. |
| [From](../processor/from/)(const System::String\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&) | Entfernt leere Seiten aus dem Dokument und speichert die Ausgabe. Gibt eine Liste der Seitenzahlen zurück, die entfernt wurden. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Entfernt leere Seiten aus dem Dokument und speichert die Ausgabe im angegebenen Format. Gibt eine Liste der Seitenzahlen zurück, die entfernt wurden. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Entfernt leere Seiten aus dem Dokument und speichert die Ausgabe im angegebenen Format. Gibt eine Liste der Seitenzahlen zurück, die entfernt wurden. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Entfernt leere Seiten aus einem Dokument, das in einem Eingabestream bereitgestellt wird, und speichert das aktualisierte Dokument in einem Ausgabestream im angegebenen Speicherformat. Gibt eine Liste der Seitenzahlen zurück, die entfernt wurden. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Entfernt leere Seiten aus einem Dokument, das in einem Eingabestream bereitgestellt wird, und speichert das aktualisierte Dokument in einem Ausgabestream im angegebenen Speicherformat. Gibt eine Liste der Seitenzahlen zurück, die entfernt wurden. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Teilt ein Dokument anhand der angegebenen Aufteilungsoptionen in mehrere Teile und speichert die resultierenden Teile in Dateien. Das Ausgabe-Dateiformat wird durch die Erweiterung des Ausgabedateinamens bestimmt. |
| static [Split](./split/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Teilt ein Dokument anhand der angegebenen Aufteilungsoptionen in mehrere Teile und speichert die resultierenden Teile in Dateien im angegebenen Speicherformat. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Teilt ein Dokument anhand der angegebenen Aufteilungsoptionen in mehrere Teile und speichert die resultierenden Teile in Dateien im angegebenen Speicherformat. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Teilt ein Dokument aus einem Eingabestream anhand der angegebenen Aufteilungsoptionen in mehrere Teile und gibt die resultierenden Teile als Array von Streams im angegebenen Speicherformat zurück. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Teilt ein Dokument aus einem Eingabestream anhand der angegebenen Aufteilungsoptionen in mehrere Teile und gibt die resultierenden Teile als Array von Streams im angegebenen Speicherformat zurück. |
| [To](../processor/to/)(const System::String\&) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Gibt den Ausgabestream für den Prozessor an. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Gibt den Ausgabestream für den Prozessor an. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Siehe auch

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
