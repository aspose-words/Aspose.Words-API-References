---
title: Splitter Class
linktitle: Splitter
articleTitle: Splitter
second_title: Aspose.Words per .NET
description: Suddividi i documenti senza sforzo con la classe Aspose.Words.LowCode.Splitter. Utilizza metodi versatili per una gestione precisa dei documenti e una maggiore efficienza del flusso di lavoro.
type: docs
weight: 4420
url: /it/net/aspose.words.lowcode/splitter/
---
## Splitter class

Fornisce metodi volti a suddividere i documenti in parti utilizzando criteri diversi.

```csharp
public class Splitter : Processor
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| static [Create](../../aspose.words.lowcode/splitter/create/)(*[SplitterContext](../splittercontext/)*) | Crea una nuova istanza del processore splitter. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Esegue l'azione del processore. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Specifica il documento di input per l'elaborazione. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Specifica il documento di input per l'elaborazione. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Specifica l'elenco dei flussi di documenti di output. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifica l'elenco dei flussi di documenti di output. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Specifica il flusso di output per il processore. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifica il flusso di output per il processore. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Specifica il file di output per il processore. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifica il file di output per il processore. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_4)(*string, string, int, int*) | Estrae un intervallo specificato di pagine da un file di documento e salva le pagine estratte in un nuovo file. Il formato del file di output è determinato dall'estensione del nome del file di output. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), int, int*) | Estrae un intervallo specificato di pagine da un flusso di documenti e salva le pagine estratte in un flusso di output utilizzando il formato di salvataggio specificato. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | Estrae un intervallo specificato di pagine da un flusso di documenti e salva le pagine estratte in un flusso di output utilizzando il formato di salvataggio specificato. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_2)(*string, string, [SaveFormat](../../aspose.words/saveformat/), int, int*) | Estrae un intervallo specificato di pagine da un file di documento e salva le pagine estratte in un nuovo file utilizzando il formato di salvataggio specificato. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_3)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | Estrae un intervallo specificato di pagine da un file di documento e salva le pagine estratte in un nuovo file utilizzando il formato di salvataggio specificato. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_2)(*string, string*) | Rimuove le pagine vuote dal documento e salva l'output. Restituisce un elenco dei numeri di pagina rimossi. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Rimuove le pagine vuote da un documento fornito in un flusso di input e salva il documento aggiornato in un flusso di output nel formato di salvataggio specificato. Restituisce un elenco dei numeri di pagina rimossi. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Rimuove le pagine vuote da un documento fornito in un flusso di input e salva il documento aggiornato in un flusso di output nel formato di salvataggio specificato. Restituisce un elenco dei numeri di pagina rimossi. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Rimuove le pagine vuote dal documento e salva l'output nel formato specificato. Restituisce un elenco dei numeri di pagina rimossi. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Rimuove le pagine vuote dal documento e salva l'output nel formato specificato. Restituisce un elenco dei numeri di pagina rimossi. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split)(*Stream, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | Divide un documento da un flusso di input in più parti in base alle opzioni di divisione specificate e restituisce le parti risultanti come una matrice di flussi nel formato di salvataggio specificato. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | Divide un documento da un flusso di input in più parti in base alle opzioni di divisione specificate e restituisce le parti risultanti come una matrice di flussi nel formato di salvataggio specificato. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_2)(*string, string, [SplitOptions](../splitoptions/)*) | Divide un documento in più parti in base alle opzioni di divisione specificate e salva le parti risultanti in file. Il formato del file di output è determinato dall'estensione del nome del file di output. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | Divide un documento in più parti in base alle opzioni di divisione specificate e salva le parti risultanti in file nel formato di salvataggio specificato. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | Divide un documento in più parti in base alle opzioni di divisione specificate e salva le parti risultanti in file nel formato di salvataggio specificato. |

### Guarda anche

* class [Processor](../processor/)
* spazio dei nomi [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../)
