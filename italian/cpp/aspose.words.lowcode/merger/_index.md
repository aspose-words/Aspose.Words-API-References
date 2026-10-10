---
title: "Classe Aspose::Words::LowCode::Merger"
linktitle: "Merger"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::LowCode::Merger. Rappresenta un gruppo di metodi destinati a unire una varietà di diversi tipi di documenti in un unico documento di output in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.lowcode/merger/
---
## Merger class


Rappresenta un gruppo di metodi destinati a unire una varietà di diversi tipi di documenti in un unico documento di output.

```cpp
class Merger : public Aspose::Words::LowCode::Processor
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| static [Create](./create/)() | Crea una nuova istanza del processore di unione della posta. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::MergerContext\>\&) | Crea una nuova istanza del processore di unione della posta. |
| [Execute](../processor/execute/)() | Esegui l'azione del processore. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Esegui l'azione del processore consentendo l'annullamento dell'attività di elaborazione del documento utilizzando il token di cancellazione specificato. |
| [From](../processor/from/)(const System::String\&) | Specifica il documento di input per l'elaborazione. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Specifica il documento di input per l'elaborazione. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Specifica il documento di input per l'elaborazione. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Specifica il documento di input per l'elaborazione. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Unisce i documenti di input forniti in un unico documento di output utilizzando i nomi di file di input e output specificati con [KeepSourceFormatting](../mergeformatmode/). |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, Aspose::Words::SaveFormat, Aspose::Words::LowCode::MergeFormatMode) | Unisce i documenti di input forniti in un unico documento di output utilizzando i nomi di file di input e output specificati e il formato finale del documento. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Unisce i documenti di input forniti in un unico documento di output utilizzando i nomi di file di input e output specificati e le opzioni di salvataggio. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Unisce i documenti di input forniti in un unico documento di output utilizzando i nomi di file di input e output specificati e le opzioni di salvataggio. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, Aspose::Words::LowCode::MergeFormatMode) | Unisce i documenti di input forniti in un unico documento e restituisce l'istanza [Document](../../aspose.words/document/) del documento finale. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Unisce i documenti di input forniti in un unico documento e restituisce l'istanza [Document](../../aspose.words/document/) del documento finale. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Unisce i documenti di input forniti in un unico documento e restituisce l'istanza [Document](../../aspose.words/document/) del documento finale. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::SaveFormat) | Unisce i documenti di input forniti in un unico documento di output utilizzando i flussi di input e output specificati e il formato finale del documento. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Unisce i documenti di input forniti in un unico documento di output utilizzando i flussi di input e output specificati e le opzioni di salvataggio. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Unisce i documenti di input forniti in un unico documento di output utilizzando i flussi di input e output specificati e le opzioni di salvataggio. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Unisce i documenti di input forniti in un unico documento e restituisce l'istanza [Document](../../aspose.words/document/) del documento finale. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Unisce i documenti di input forniti in un unico documento e restituisce l'istanza [Document](../../aspose.words/document/) del documento finale. |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Unisce i documenti di input forniti in un unico documento di output utilizzando i nomi di file di input e output specificati e le opzioni di salvataggio. Renderizza l'output in immagini. |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Unisce i flussi di documenti di input forniti in un unico documento di output utilizzando le opzioni di salvataggio immagine specificate. Renderizza l'output in immagini. |
| [To](../processor/to/)(const System::String\&) | Specifica il file di output per il processore. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Specifica il file di output per il processore. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Specifica il file di output per il processore. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Specifica il flusso di output per il processore. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Specifica il flusso di output per il processore. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Note


I file o i flussi di input e output specificati, insieme alle opzioni di unione e salvataggio desiderate, vengono utilizzati per unire i documenti di input forniti in un unico documento di output.

La funzionalità di unione supporta oltre 35 diversi formati di file.
## Vedi anche

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
