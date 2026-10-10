---
title: "Classe Aspose::Words::LowCode::Splitter"
linktitle: "Splitter"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::LowCode::Splitter. Fornisce metodi destinati a suddividere i documenti in parti usando diversi criteri in C++."
type: docs
weight: 1500
url: /it/cpp/aspose.words.lowcode/splitter/
---
## Splitter class


Fornisce metodi destinati a suddividere i documenti in parti utilizzando criteri diversi.

```cpp
class Splitter : public Aspose::Words::LowCode::Processor
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::SplitterContext\>\&) | Crea una nuova istanza del processore splitter. |
| [Execute](../processor/execute/)() | Esegui l'azione del processore. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Esegui l'azione del processore consentendo l'annullamento dell'attività di elaborazione del documento utilizzando il token di cancellazione specificato. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, int32_t, int32_t) | Estrae un intervallo specificato di pagine da un file documento e salva le pagine estratte in un nuovo file. Il formato del file di output è determinato dall'estensione del nome del file di output. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) | Estrae un intervallo specificato di pagine da un file documento e salva le pagine estratte in un nuovo file utilizzando il formato di salvataggio specificato. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | Estrae un intervallo specificato di pagine da un file documento e salva le pagine estratte in un nuovo file utilizzando il formato di salvataggio specificato. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) | Estrae un intervallo specificato di pagine da un flusso di documento e salva le pagine estratte in un flusso di output usando il formato di salvataggio specificato. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | Estrae un intervallo specificato di pagine da un flusso di documento e salva le pagine estratte in un flusso di output usando il formato di salvataggio specificato. |
| [From](../processor/from/)(const System::String\&) | Specifica il documento di input per l'elaborazione. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Specifica il documento di input per l'elaborazione. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Specifica il documento di input per l'elaborazione. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Specifica il documento di input per l'elaborazione. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&) | Rimuove le pagine vuote dal documento e salva l'output. Restituisce un elenco di numeri di pagina che sono stati rimossi. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Rimuove le pagine vuote dal documento e salva l'output nel formato specificato. Restituisce un elenco di numeri di pagina che sono stati rimossi. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Rimuove le pagine vuote dal documento e salva l'output nel formato specificato. Restituisce un elenco di numeri di pagina che sono stati rimossi. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Rimuove le pagine bianche da un documento fornito in un flusso di input e salva il documento aggiornato in un flusso di output nel formato di salvataggio specificato. Restituisce un elenco di numeri di pagina che sono stati rimossi. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Rimuove le pagine bianche da un documento fornito in un flusso di input e salva il documento aggiornato in un flusso di output nel formato di salvataggio specificato. Restituisce un elenco di numeri di pagina che sono stati rimossi. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Divide un documento in più parti in base alle opzioni di divisione specificate e salva le parti risultanti in file. Il formato del file di output è determinato dall'estensione del nome del file di output. |
| static [Split](./split/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Divide un documento in più parti in base alle opzioni di divisione specificate e salva le parti risultanti in file nel formato di salvataggio specificato. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Divide un documento in più parti in base alle opzioni di divisione specificate e salva le parti risultanti in file nel formato di salvataggio specificato. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Divide un documento da un flusso di input in più parti in base alle opzioni di divisione specificate e restituisce le parti risultanti come un array di flussi nel formato di salvataggio specificato. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Divide un documento da un flusso di input in più parti in base alle opzioni di divisione specificate e restituisce le parti risultanti come un array di flussi nel formato di salvataggio specificato. |
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
