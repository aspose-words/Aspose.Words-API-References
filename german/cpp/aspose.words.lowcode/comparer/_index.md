---
title: "Aspose::Words::LowCode::Comparer Klasse"
linktitle: "Comparer"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::Comparer class. Stellt Methoden bereit, die zum Vergleichen von Dokumenten in C++ vorgesehen sind."
type: docs
weight: 500
url: /de/cpp/aspose.words.lowcode/comparer/
---
## Comparer class


Stellt Methoden bereit, die zum Vergleichen von Dokumenten vorgesehen sind.

```cpp
class Comparer : public Aspose::Words::LowCode::Processor
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) | Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei im angegebenen Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei im angegebenen Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) | Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei im angegebenen Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei im angegebenen Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | Vergleicht zwei Dokumente, die aus Streams geladen wurden, mit zusätzlichen Optionen und speichert die Unterschiede in den bereitgestellten Ausgabestream im angegebenen Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Vergleicht zwei Dokumente, die aus Streams geladen wurden, mit zusätzlichen Optionen und speichert die Unterschiede in den bereitgestellten Ausgabestream im angegebenen Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) | Vergleicht zwei Dokumente, die aus Streams geladen wurden, mit zusätzlichen Optionen und speichert die Unterschiede in den bereitgestellten Ausgabestream im angegebenen Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Vergleicht zwei Dokumente, die aus Streams geladen wurden, mit zusätzlichen Optionen und speichert die Unterschiede in den bereitgestellten Ausgabestream im angegebenen Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs- und Formatierungsrevisionen erzeugt werden. |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) | Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. Jeder Eintrag im zurückgegebenen Array stellt eine einzelne Seite der Ausgabe dar, die als Bild gerendert wird. |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. Jeder Eintrag im zurückgegebenen Array stellt eine einzelne Seite der Ausgabe dar, die als Bild gerendert wird. |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) | Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. Jeder Eintrag im zurückgegebenen Array stellt eine einzelne Seite der Ausgabe dar, die als Bild gerendert wird. |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. Jeder Eintrag im zurückgegebenen Array stellt eine einzelne Seite der Ausgabe dar, die als Bild gerendert wird. |
| static [Create](./create/)() | Erstellt eine neue Instanz des Konverter‑Prozessors. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ComparerContext\>\&) | Erstellt eine neue Instanz des Comparer‑Prozessors. |
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
## Siehe auch

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
