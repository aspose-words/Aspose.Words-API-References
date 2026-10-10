---
title: "Aspose::Words::LowCode::Processor Klasse"
linktitle: "Processor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::Processor Klasse. Prozessor-Klasse zur Durchführung verschiedener Dokumentenverarbeitungsaktionen in C++."
type: docs
weight: 1126
url: /de/cpp/aspose.words.lowcode/processor/
---
## Processor class


[Processor](./) class for performing different document processing actions.

```cpp
class Processor : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Execute](./execute/)() | Führt die Prozessoraktion aus. |
| [Execute](./execute/)(System::Threading::CancellationToken) | Führt die Prozessoraktion aus und ermöglicht das Abbrechen des Dokumentverarbeitungsvorgangs mithilfe des angegebenen Abbruchtokens. |
| [From](./from/)(const System::String\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](./from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](./from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](./from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Gibt das Eingabedokument für die Verarbeitung an. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [To](./to/)(const System::String\&) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](./to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](./to/)(const System::String\&, Aspose::Words::SaveFormat) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](./to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Gibt den Ausgabestream für den Prozessor an. |
| [To](./to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Gibt den Ausgabestream für den Prozessor an. |
| [To](./to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](./to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
