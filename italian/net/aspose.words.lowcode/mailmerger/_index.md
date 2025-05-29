---
title: MailMerger Class
linktitle: MailMerger
articleTitle: MailMerger
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.LowCode.MailMerger. Riempi i modelli di dati senza sforzo utilizzando tecniche di stampa unione semplici e avanzate per un'automazione impeccabile dei documenti.
type: docs
weight: 4270
url: /it/net/aspose.words.lowcode/mailmerger/
---
## MailMerger class

Fornisce metodi volti a riempire il modello con dati utilizzando operazioni di unione di posta semplice e unione di posta con regioni.

```csharp
public class MailMerger : Processor
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| static [Create](../../aspose.words.lowcode/mailmerger/create/)(*[MailMergerContext](../mailmergercontext/)*) | Crea una nuova istanza del processore di stampa unione. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Esegue l'azione del processore. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Specifica il documento di input per l'elaborazione. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Specifica il documento di input per l'elaborazione. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Specifica l'elenco dei flussi di documenti di output. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifica l'elenco dei flussi di documenti di output. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Specifica il flusso di output per il processore. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifica il flusso di output per il processore. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Specifica il file di output per il processore. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifica il file di output per il processore. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_12)(*string, string, DataRow*) | Esegue la stampa unione da un DataRow nel documento. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_13)(*string, string, DataTable*) | Esegue la stampa unione da una tabella dati nel documento. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_14)(*string, string, string[], object[]*) | Esegue un'operazione di unione di posta per un singolo record. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Esegue un'operazione di unione di posta per un singolo record. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Esegue un'operazione di unione di posta per un singolo record. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Esegue un'operazione di unione di posta per un singolo record. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_4)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Esegue un'operazione di unione di posta per un singolo record. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_6)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Esegue la stampa unione da un DataRow nel documento. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_7)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Esegue la stampa unione da un DataRow nel documento. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_9)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Esegue la stampa unione da un DataRow nel documento. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_10)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Esegue la stampa unione da un DataRow nel documento. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_2)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Esegue un'operazione di unione di posta per un singolo record. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_5)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Esegue un'operazione di unione di posta per un singolo record. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_8)(*string, string, [SaveFormat](../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Esegue un'operazione di unione di posta per un singolo record. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_11)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Esegue un'operazione di unione di posta per un singolo record. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Esegue la stampa unione da un DataRow nel documento e restituisce il risultato in immagini. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_1)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Esegue la stampa unione da un DataRow nel documento e restituisce il risultato in immagini. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_3)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Esegue la stampa unione da un DataRow nel documento e restituisce il risultato in immagini. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_4)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Esegue la stampa unione da un DataRow nel documento e restituisce il risultato in immagini. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_2)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Esegue un'operazione di unione di posta per un singolo record e restituisce il risultato in immagini. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_5)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Esegue un'operazione di unione di posta per un singolo record e restituisce il risultato in immagini. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_8)(*string, string, DataSet*) | Esegue la stampa unione da un DataSet in un documento con aree di stampa unione. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_9)(*string, string, DataTable*) | Esegue la stampa unione da una tabella dati nel documento con aree di stampa unione. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Esegue la stampa unione da un DataSet nel documento con aree di stampa unione. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Esegue un'operazione di unione di posta per un singolo record. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_2)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Esegue la stampa unione da un DataSet nel documento con aree di stampa unione. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Esegue un'operazione di unione di posta per un singolo record. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_4)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Esegue la stampa unione da un DataSet nel documento con aree di stampa unione. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_5)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Esegue la stampa unione da una tabella dati nel documento con aree di stampa unione. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_6)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Esegue la stampa unione da un DataSet nel documento con aree di stampa unione. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_7)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Esegue la stampa unione da una tabella dati nel documento con aree di stampa unione. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Esegue la stampa unione da un DataSet nel documento con aree di stampa unione e restituisce il risultato in immagini. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages_1)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Esegue la stampa unione da un DataTable nel documento con aree di stampa unione e restituisce il risultato in immagini. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages_2)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Esegue la stampa unione da un DataSet nel documento con aree di stampa unione e restituisce il risultato in immagini. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages_3)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Esegue la stampa unione da un DataTable nel documento con aree di stampa unione e restituisce il risultato in immagini. |

### Guarda anche

* class [Processor](../processor/)
* spazio dei nomi [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../)
