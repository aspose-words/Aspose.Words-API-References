---
title: "classe Aspose::Words::LowCode::Processor"
linktitle: "Processor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::LowCode::Processor. Classe di elaborazione per eseguire diverse azioni di elaborazione dei documenti in C++."
type: docs
weight: 1126
url: /it/cpp/aspose.words.lowcode/processor/
---
## Processor class


[Processor](./) class for performing different document processing actions.

```cpp
class Processor : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Execute](./execute/)() | Esegui l'azione del processore. |
| [Execute](./execute/)(System::Threading::CancellationToken) | Esegui l'azione del processore consentendo l'annullamento dell'attività di elaborazione del documento utilizzando il token di cancellazione specificato. |
| [From](./from/)(const System::String\&) | Specifica il documento di input per l'elaborazione. |
| [From](./from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Specifica il documento di input per l'elaborazione. |
| [From](./from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Specifica il documento di input per l'elaborazione. |
| [From](./from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Specifica il documento di input per l'elaborazione. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [To](./to/)(const System::String\&) | Specifica il file di output per il processore. |
| [To](./to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Specifica il file di output per il processore. |
| [To](./to/)(const System::String\&, Aspose::Words::SaveFormat) | Specifica il file di output per il processore. |
| [To](./to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Specifica il flusso di output per il processore. |
| [To](./to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Specifica il flusso di output per il processore. |
| [To](./to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](./to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
