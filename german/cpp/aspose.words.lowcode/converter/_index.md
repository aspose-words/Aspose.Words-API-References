---
title: "Aspose::Words::LowCode::Converter Klasse"
linktitle: "Converter"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::Converter Klasse. Stellt eine Gruppe von Methoden dar, die dazu bestimmt sind, verschiedene Dokumenttypen mit einer einzigen Codezeile in C++ zu konvertieren."
type: docs
weight: 600
url: /de/cpp/aspose.words.lowcode/converter/
---
## Converter class


Stellt eine Gruppe von Methoden dar, die dazu bestimmt sind, verschiedene Dokumenttypen mit einer einzigen Codezeile zu konvertieren.

```cpp
class Converter : public Aspose::Words::LowCode::Processor
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| static [Convert](./convert/)(const System::String\&, const System::String\&) | Konvertiert das angegebene Eingabedokument in das Ausgabedokument unter Verwendung der angegebenen Eingabe- und Ausgabedateinamen sowie deren Erweiterungen. |
| static [Convert](./convert/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Konvertiert das angegebene Eingabedokument in das Ausgabedokument unter Verwendung der angegebenen Eingabe- und Ausgabedateinamen und des endgültigen Dokumentformats. |
| static [Convert](./convert/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Konvertiert das angegebene Eingabedokument in das Ausgabedokument unter Verwendung der angegebenen Eingabe- und Ausgabedateinamen sowie der Speicheroptionen. |
| static [Convert](./convert/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Konvertiert das angegebene Eingabedokument in das Ausgabedokument unter Verwendung der angegebenen Eingabe- und Ausgabedateinamen sowie seiner Lade-/Speicheroptionen. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Konvertiert das angegebene Eingabedokument in ein einzelnes Ausgabedokument unter Verwendung der angegebenen Eingabe- und Ausgabeströme. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Konvertiert das angegebene Eingabedokument in ein einzelnes Ausgabedokument unter Verwendung der angegebenen Eingabe- und Ausgabeströme. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Konvertiert das angegebene Eingabedokument in ein einzelnes Ausgabedokument unter Verwendung der angegebenen Eingabe- und Ausgabeströme. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&) | Konvertiert die Seiten der angegebenen Eingabedatei in Bilddateien. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Konvertiert die Seiten der angegebenen Eingabedatei in Bilddateien im angegebenen Format. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Konvertiert die Seiten der angegebenen Eingabedatei in Bilddateien unter Verwendung der angegebenen Speicheroptionen. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Konvertiert die Seiten der angegebenen Eingabedatei in Bilddateien unter Verwendung der bereitgestellten Lade- und Speicheroptionen. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, Aspose::Words::SaveFormat) | Konvertiert die Seiten der angegebenen Eingabedatei in Bilder im angegebenen Format und gibt ein Array von Streams zurück, das die Bilder enthält. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Konvertiert die Seiten der angegebenen Eingabedatei in Bilder unter Verwendung der angegebenen Speicheroptionen und gibt ein Array von Streams zurück, das die Bilder enthält. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Konvertiert die Seiten des angegebenen Eingabestreams in Bilder im angegebenen Format und gibt ein Array von Streams zurück, das die Bilder enthält. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Konvertiert die Seiten des angegebenen Eingabestreams in Bilder unter Verwendung der angegebenen Speicheroptionen und gibt ein Array von Streams zurück, das die Bilder enthält. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Konvertiert die Seiten des angegebenen Eingabestreams in Bilder unter Verwendung der bereitgestellten Lade- und Speicheroptionen und gibt ein Array von Streams zurück, das die Bilder enthält. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::SaveFormat) | Konvertiert die Seiten des angegebenen Dokuments in Bilder im angegebenen Format und gibt ein Array von Streams zurück, das die Bilder enthält. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Konvertiert die Seiten des angegebenen Dokuments in Bilder unter Verwendung der angegebenen Speicheroptionen und gibt ein Array von Streams zurück, das die Bilder enthält. |
| static [Create](./create/)() | Erstellt eine neue Instanz des Konverter‑Prozessors. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ConverterContext\>\&) | Erstellt eine neue Instanz des Konverter‑Prozessors. |
| [Execute](../processor/execute/)() | Führt die Prozessoraktion aus. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Führt die Prozessoraktion aus und ermöglicht das Abbrechen des Dokumentverarbeitungsvorgangs mithilfe des angegebenen Abbruchtokens. |
| [From](../processor/from/)(const System::String\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [To](../processor/to/)(const System::String\&) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Gibt den Ausgabestream für den Prozessor an. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Gibt den Ausgabestream für den Prozessor an. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Hinweise


Die angegebenen Eingabe- und Ausgabedateien oder -streams sowie das gewünschte Speicherformat werden verwendet, um das gegebene Eingabedokument des einen Formats in das Ausgabedokument des anderen angegebenen Formats zu konvertieren.

Die Konvertierungsfunktion unterstützt über 35+ verschiedene Dateiformate.

Die [ConvertToImages()](../)-Gruppe von Methoden ist dafür ausgelegt, Dokumente in Bilder zu verwandeln, wobei jede Seite in eine separate Bilddatei konvertiert wird. Diese Methoden konvertieren PDF‑Dokumente außerdem direkt in feste Seitenformate, ohne sie in das Dokumentenmodell zu laden, was sowohl die Leistung als auch die Genauigkeit verbessert.

Mit [PageSet](../../aspose.words.saving/imagesaveoptions/get_pageset/) können Sie einen bestimmten Satz von Seiten angeben, die in Bilder konvertiert werden sollen.
## Siehe auch

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
