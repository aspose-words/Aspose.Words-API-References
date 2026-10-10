---
title: "Classe Aspose::Words::LowCode::Converter"
linktitle: "Converter"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::LowCode::Converter. Rappresenta un gruppo di metodi destinati a convertire una varietà di diversi tipi di documenti usando una singola riga di codice in C++."
type: docs
weight: 600
url: /it/cpp/aspose.words.lowcode/converter/
---
## Converter class


Rappresenta un gruppo di metodi destinati a convertire una varietà di diversi tipi di documenti usando una singola riga di codice.

```cpp
class Converter : public Aspose::Words::LowCode::Processor
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| static [Convert](./convert/)(const System::String\&, const System::String\&) | Converte il documento di input fornito nel documento di output utilizzando i nomi dei file di input e output specificati e le relative estensioni. |
| static [Convert](./convert/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Converte il documento di input fornito nel documento di output utilizzando i nomi di file di input e output specificati e il formato finale del documento. |
| static [Convert](./convert/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Converte il documento di input fornito nel documento di output utilizzando i nomi di file di input e output specificati e le opzioni di salvataggio. |
| static [Convert](./convert/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Converte il documento di input fornito nel documento di output utilizzando i nomi di file di input e output specificati e le sue opzioni di caricamento/salvataggio. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Converte il documento di input fornito in un unico documento di output utilizzando i flussi di input e output specificati. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Converte il documento di input fornito in un unico documento di output utilizzando i flussi di input e output specificati. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Converte il documento di input fornito in un unico documento di output utilizzando i flussi di input e output specificati. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&) | Converte le pagine del file di input specificato in file immagine. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Converte le pagine del file di input specificato in file immagine nel formato specificato. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Converte le pagine del file di input specificato in file immagine utilizzando le opzioni di salvataggio specificate. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Converte le pagine del file di input specificato in file immagine utilizzando le opzioni di caricamento e salvataggio fornite. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, Aspose::Words::SaveFormat) | Converte le pagine del file di input specificato in immagini nel formato specificato e restituisce un array di flussi contenenti le immagini. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Converte le pagine del file di input specificato in immagini utilizzando le opzioni di salvataggio specificate e restituisce un array di flussi contenenti le immagini. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Converte le pagine del flusso di input specificato in immagini nel formato specificato e restituisce un array di flussi contenenti le immagini. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Converte le pagine del flusso di input specificato in immagini utilizzando le opzioni di salvataggio specificate e restituisce un array di flussi contenenti le immagini. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Converte le pagine del flusso di input specificato in immagini utilizzando le opzioni di caricamento e salvataggio fornite, e restituisce un array di flussi contenenti le immagini. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::SaveFormat) | Converte le pagine del documento specificato in immagini nel formato specificato e restituisce un array di flussi contenenti le immagini. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Converte le pagine del documento specificato in immagini utilizzando le opzioni di salvataggio specificate e restituisce un array di flussi contenenti le immagini. |
| static [Create](./create/)() | Crea una nuova istanza del processore convertitore. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ConverterContext\>\&) | Crea una nuova istanza del processore convertitore. |
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
## Note


I file o i flussi di input e output specificati, insieme al formato di salvataggio desiderato, vengono utilizzati per convertire il documento di input fornito da un formato in quello di output nell'altro formato specificato.

La funzionalità di conversione supporta oltre 35 diversi formati di file.

Il gruppo di metodi [ConvertToImages()](../) è progettato per trasformare i documenti in immagini, con ogni pagina convertita in un file immagine separato. Questi metodi convertono anche i documenti PDF direttamente in formati a pagina fissa senza caricarli nel modello del documento, il che migliora sia le prestazioni sia l'accuratezza.

Con [PageSet](../../aspose.words.saving/imagesaveoptions/get_pageset/), è possibile specificare un insieme particolare di pagine da convertire in immagini.
## Vedi anche

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
