---
title: Merger Class
linktitle: Merger
articleTitle: Merger
second_title: Aspose.Words per .NET
description: Unisci senza sforzo diversi tipi di documenti in uno solo con la classe Aspose.Words.LowCode.Merger. Semplifica il tuo flusso di lavoro e aumenta la produttività oggi stesso!
type: docs
weight: 4300
url: /it/net/aspose.words.lowcode/merger/
---
## Merger class

Rappresenta un gruppo di metodi volti a unire diversi tipi di documenti in un unico documento di output.

```csharp
public class Merger : Processor
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| static [Create](../../aspose.words.lowcode/merger/create/#create)() | Crea una nuova istanza del processore di stampa unione. |
| static [Create](../../aspose.words.lowcode/merger/create/#create_1)(*[MergerContext](../mergercontext/)*) | Crea una nuova istanza del processore di stampa unione. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Esegue l'azione del processore. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Specifica il documento di input per l'elaborazione. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Specifica il documento di input per l'elaborazione. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Specifica l'elenco dei flussi di documenti di output. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifica l'elenco dei flussi di documenti di output. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Specifica il flusso di output per il processore. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifica il flusso di output per il processore. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Specifica il file di output per il processore. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifica il file di output per il processore. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge)(*Document[], [MergeFormatMode](../mergeformatmode/)*) | Unisce i documenti di input specificati in un unico documento e restituisce[`Document`](../../aspose.words/document/) istanza del documento finale. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_2)(*Stream[], [MergeFormatMode](../mergeformatmode/)*) | Unisce i documenti di input specificati in un unico documento e restituisce[`Document`](../../aspose.words/document/) istanza del documento finale. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_8)(*string, string[]*) | Unisce i documenti di input specificati in un singolo documento di output utilizzando input e nomi di file di output specificati utilizzandoKeepSourceFormatting . |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_4)(*string[], [MergeFormatMode](../mergeformatmode/)*) | Unisce i documenti di input specificati in un unico documento e restituisce[`Document`](../../aspose.words/document/) istanza del documento finale. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_6)(*Stream, Stream[], [SaveFormat](../../aspose.words/saveformat/)*) | Unisce i documenti di input specificati in un singolo documento di output utilizzando i flussi di input e output specificati e il formato del documento finale. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_1)(*Stream[], LoadOptions[], [MergeFormatMode](../mergeformatmode/)*) | Unisce i documenti di input specificati in un unico documento e restituisce[`Document`](../../aspose.words/document/) istanza del documento finale. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_3)(*string[], LoadOptions[], [MergeFormatMode](../mergeformatmode/)*) | Unisce i documenti di input specificati in un unico documento e restituisce[`Document`](../../aspose.words/document/) istanza del documento finale. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_7)(*Stream, Stream[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Unisce i documenti di input specificati in un singolo documento di output utilizzando flussi di input e output specificati e opzioni di salvataggio. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_10)(*string, string[], [SaveFormat](../../aspose.words/saveformat/), [MergeFormatMode](../mergeformatmode/)*) | Unisce i documenti di input specificati in un singolo documento di output utilizzando i nomi dei file di input e output specificati e il formato del documento finale. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_11)(*string, string[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Unisce i documenti di input specificati in un singolo documento di output utilizzando i nomi dei file di input e output specificati e le opzioni di salvataggio. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_5)(*Stream, Stream[], LoadOptions[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Unisce i documenti di input specificati in un singolo documento di output utilizzando flussi di input e output specificati e opzioni di salvataggio. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_9)(*string, string[], LoadOptions[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Unisce i documenti di input specificati in un singolo documento di output utilizzando i nomi dei file di input e output specificati e le opzioni di salvataggio. |
| static [MergeToImages](../../aspose.words.lowcode/merger/mergetoimages/#mergetoimages)(*Stream[], [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Unisce i flussi di documenti di input specificati in un singolo documento di output utilizzando le opzioni di salvataggio delle immagini specificate. Esegue il rendering dell'output in immagini. |
| static [MergeToImages](../../aspose.words.lowcode/merger/mergetoimages/#mergetoimages_1)(*string[], [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Unisce i documenti di input specificati in un singolo documento di output utilizzando i nomi dei file di input e output specificati e le opzioni di salvataggio. Esegue il rendering dell'output in immagini. |

## Osservazioni

I file o flussi di input e output specificati, insieme alle opzioni di unione e salvataggio desiderate, vengono utilizzati per unire i documenti di input specificati in un singolo documento di output.

La funzionalità di unione supporta oltre 35 formati di file diversi.

## Esempi

Mostra come unire i documenti in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Guarda anche

* class [Processor](../processor/)
* spazio dei nomi [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../)
