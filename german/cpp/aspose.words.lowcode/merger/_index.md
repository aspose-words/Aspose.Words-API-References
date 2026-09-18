---
title: "Aspose::Words::LowCode::Merger Klasse"
linktitle: "Zusammenführer"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::Merger Klasse. Stellt eine Gruppe von Methoden dar, die dazu bestimmt sind, verschiedene Dokumenttypen zu einem einzigen Ausgabedokument in C++ zusammenzuführen."
type: docs
weight: 1000
url: /de/cpp/aspose.words.lowcode/merger/
---
## Merger class


Stellt eine Gruppe von Methoden dar, die dazu bestimmt sind, verschiedene Dokumenttypen zu einem einzigen Ausgabedokument zusammenzuführen.

```cpp
class Merger : public Aspose::Words::LowCode::Processor
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| static [Create](./create/)() | Erstellt eine neue Instanz des Mail-Merger-Prozessors. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::MergerContext\>\&) | Erstellt eine neue Instanz des Mail-Merger-Prozessors. |
| [Execute](../processor/execute/)() | Führt die Prozessoraktion aus. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Führt die Prozessoraktion aus und ermöglicht das Abbrechen des Dokumentverarbeitungsvorgangs mithilfe des angegebenen Abbruchtokens. |
| [From](../processor/from/)(const System::String\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Führt die angegebenen Eingabedokumente zu einem einzigen Ausgabedokument zusammen, wobei die angegebenen Eingabe- und Ausgabedateinamen verwendet werden, und nutzt dabei [KeepSourceFormatting](../mergeformatmode/). |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, Aspose::Words::SaveFormat, Aspose::Words::LowCode::MergeFormatMode) | Führt die angegebenen Eingabedokumente zu einem einzigen Ausgabedokument zusammen, wobei die angegebenen Eingabe- und Ausgabedateinamen sowie das endgültige Dokumentformat verwendet werden. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Führt die angegebenen Eingabedokumente zu einem einzigen Ausgabedokument zusammen, wobei die angegebenen Eingabe- und Ausgabedateinamen und Speicheroptionen verwendet werden. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Führt die angegebenen Eingabedokumente zu einem einzigen Ausgabedokument zusammen, wobei die angegebenen Eingabe- und Ausgabedateinamen und Speicheroptionen verwendet werden. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, Aspose::Words::LowCode::MergeFormatMode) | Führt die angegebenen Eingabedokumente zu einem einzigen Dokument zusammen und gibt eine [Document](../../aspose.words/document/) Instanz des endgültigen Dokuments zurück. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Führt die angegebenen Eingabedokumente zu einem einzigen Dokument zusammen und gibt eine [Document](../../aspose.words/document/) Instanz des endgültigen Dokuments zurück. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Führt die angegebenen Eingabedokumente zu einem einzigen Dokument zusammen und gibt eine [Document](../../aspose.words/document/) Instanz des endgültigen Dokuments zurück. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::SaveFormat) | Führt die angegebenen Eingabedokumente zu einem einzigen Ausgabedokument zusammen, wobei die angegebenen Eingabe- und Ausgabeströme sowie das endgültige Dokumentformat verwendet werden. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Führt die angegebenen Eingabedokumente zu einem einzigen Ausgabedokument zusammen, wobei die angegebenen Eingabe- und Ausgabeströme und Speicheroptionen verwendet werden. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Führt die angegebenen Eingabedokumente zu einem einzigen Ausgabedokument zusammen, wobei die angegebenen Eingabe- und Ausgabeströme und Speicheroptionen verwendet werden. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Führt die angegebenen Eingabedokumente zu einem einzigen Dokument zusammen und gibt eine [Document](../../aspose.words/document/) Instanz des endgültigen Dokuments zurück. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Führt die angegebenen Eingabedokumente zu einem einzigen Dokument zusammen und gibt eine [Document](../../aspose.words/document/) Instanz des endgültigen Dokuments zurück. |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Führt die angegebenen Eingabedokumente zu einem einzigen Ausgabedokument zusammen, wobei die angegebenen Eingabe- und Ausgabedateinamen und Speicheroptionen verwendet werden. Rendert die Ausgabe zu Bildern. |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Führt die angegebenen Eingabedokumentströme zu einem einzigen Ausgabedokument zusammen, wobei die angegebenen Bildspeicheroptionen verwendet werden. Rendert die Ausgabe zu Bildern. |
| [To](../processor/to/)(const System::String\&) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Gibt den Ausgabestream für den Prozessor an. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Gibt den Ausgabestream für den Prozessor an. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Hinweise


Die angegebenen Eingabe- und Ausgabedateien oder -ströme werden zusammen mit den gewünschten Zusammenführungs- und Speicheroptionen verwendet, um die angegebenen Eingabedokumente zu einem einzigen Ausgabedokument zusammenzuführen.

Die Zusammenführungsfunktion unterstützt über 35 verschiedene Dateiformate.
## Siehe auch

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
