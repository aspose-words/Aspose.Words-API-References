---
title: "Aspose::Words::LowCode::Comparer class"
linktitle: "Comparer"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::LowCode::Comparer class. Fornisce metodi destinati a confrontare documenti in C++."
type: docs
weight: 500
url: /it/cpp/aspose.words.lowcode/comparer/
---
## Comparer class


Fornisce metodi destinati a confrontare i documenti.

```cpp
class Comparer : public Aspose::Words::LowCode::Processor
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) | Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato, producendo modifiche come un numero di revisioni di modifica e formattazione. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato, producendo modifiche come un numero di revisioni di modifica e formattazione. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato nel formato di salvataggio fornito, producendo modifiche come un numero di revisioni di modifica e formattazione. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato nel formato di salvataggio fornito, producendo modifiche come un numero di revisioni di modifica e formattazione. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) | Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato nel formato di salvataggio fornito, producendo modifiche come un numero di revisioni di modifica e formattazione. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato nel formato di salvataggio fornito, producendo modifiche come un numero di revisioni di modifica e formattazione. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | Confronta due documenti caricati da flussi con opzioni aggiuntive e salva le differenze nel flusso di output fornito nel formato di salvataggio specificato, producendo modifiche come un numero di revisioni di modifica e formattazione. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Confronta due documenti caricati da flussi con opzioni aggiuntive e salva le differenze nel flusso di output fornito nel formato di salvataggio specificato, producendo modifiche come un numero di revisioni di modifica e formattazione. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) | Confronta due documenti caricati da flussi con opzioni aggiuntive e salva le differenze nel flusso di output fornito nel formato di salvataggio specificato, producendo modifiche come un numero di revisioni di modifica e formattazione. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Confronta due documenti caricati da flussi con opzioni aggiuntive e salva le differenze nel flusso di output fornito nel formato di salvataggio specificato, producendo modifiche come un numero di revisioni di modifica e formattazione. |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) | Confronta due documenti e salva le differenze come immagini. Ogni elemento nell'array restituito rappresenta una singola pagina dell'output renderizzata come immagine. |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Confronta due documenti e salva le differenze come immagini. Ogni elemento nell'array restituito rappresenta una singola pagina dell'output renderizzata come immagine. |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) | Confronta due documenti e salva le differenze come immagini. Ogni elemento nell'array restituito rappresenta una singola pagina dell'output renderizzata come immagine. |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Confronta due documenti e salva le differenze come immagini. Ogni elemento nell'array restituito rappresenta una singola pagina dell'output renderizzata come immagine. |
| static [Create](./create/)() | Crea una nuova istanza del processore convertitore. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ComparerContext\>\&) | Crea una nuova istanza del processore comparatore. |
| [Execute](../processor/execute/)() | Esegui l'azione del processore. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Esegui l'azione del processore consentendo l'annullamento dell'attività di elaborazione del documento utilizzando il token di cancellazione specificato. |
| [From](../processor/from/)(const System::String\&) | Specifica il documento di input per l'elaborazione. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Specifica il documento di input per l'elaborazione. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Specifica il documento di input per l'elaborazione. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Specifica il documento di input per l'elaborazione. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [To](../processor/to/)(const System::String\&) | Specifica il file di output per il processore. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Specifica il file di output per il processore. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Specifica il file di output per il processore. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Specifica il flusso di output per il processore. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Specifica il flusso di output per il processore. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Vedi anche

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
