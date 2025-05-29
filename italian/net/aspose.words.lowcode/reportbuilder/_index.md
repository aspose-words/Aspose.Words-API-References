---
title: ReportBuilder Class
linktitle: ReportBuilder
articleTitle: ReportBuilder
second_title: Aspose.Words per .NET
description: Crea report dinamici senza sforzo con Aspose.Words LowCode ReportBuilder. Utilizza LINQ Reporting Engine per riempire i modelli di dati in modo fluido.
type: docs
weight: 4360
url: /it/net/aspose.words.lowcode/reportbuilder/
---
## ReportBuilder class

Fornisce metodi destinati a riempire il modello con dati utilizzando LINQ Reporting Engine.

```csharp
public class ReportBuilder : Processor
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| static [Create](../../aspose.words.lowcode/reportbuilder/create/#create)() | Crea una nuova istanza del processore del generatore di report. |
| static [Create](../../aspose.words.lowcode/reportbuilder/create/#create_1)(*[ReportBuilderContext](../reportbuildercontext/)*) | Crea una nuova istanza del processore del generatore di report. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Esegue l'azione del processore. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Specifica il documento di input per l'elaborazione. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Specifica il documento di input per l'elaborazione. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Specifica l'elenco dei flussi di documenti di output. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifica l'elenco dei flussi di documenti di output. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Specifica il flusso di output per il processore. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifica il flusso di output per il processore. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Specifica il file di output per il processore. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifica il file di output per il processore. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_12)(*string, string, object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Popola il documento modello con i dati provenienti dalla fonte specificata, generando un report completo con opzioni aggiuntive. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Popola il documento modello con dati provenienti dalla fonte specificata, generando un report completo con il formato di output specificato e opzioni aggiuntive, dai flussi di input e output. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Popola il documento modello con dati provenienti dalla fonte specificata, generando un report completo con il formato di output specificato e opzioni aggiuntive, dai flussi di input e output. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_13)(*string, string, object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Popola il documento modello con i dati provenienti dalla fonte specificata, generando un report completo con un riferimento alla fonte dati denominata e opzioni aggiuntive. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_14)(*string, string, object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Popola il documento modello con dati provenienti da più fonti, generando un report completo con opzioni aggiuntive. Questo sovraccarico determina automaticamente il formato di salvataggio in base all'estensione del file di output. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_6)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Popola il documento modello con i dati provenienti dalla fonte specificata, generando un report completo con il formato di output specificato e opzioni aggiuntive. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_9)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Popola il documento modello con i dati provenienti dalla fonte specificata, generando un report completo con il formato di output specificato e opzioni aggiuntive. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Popola il documento modello con i dati provenienti dalla fonte specificata, generando un report completo con un riferimento alla fonte dati denominata e opzioni aggiuntive. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_2)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Popola il documento modello con dati provenienti da più fonti, generando un report completo con il formato di output specificato e opzioni aggiuntive dai flussi di file di input e output specificati. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_4)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Popola il documento modello con i dati provenienti dalla fonte specificata, generando un report completo con un riferimento alla fonte dati denominata e opzioni aggiuntive. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_5)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Popola il documento modello con dati provenienti da più fonti, generando un report completo con il formato di output specificato e opzioni aggiuntive dai flussi di file di input e output specificati. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_7)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Popola il documento modello con dati provenienti dalla fonte specificata, generando un report completo con il formato di output specificato, un riferimento alla fonte dati denominata e opzioni aggiuntive. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_8)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Popola il documento modello con dati provenienti da più fonti, generando un report completo con un formato di output specificato e opzioni aggiuntive. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_10)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Popola il documento modello con dati provenienti dalla fonte specificata, generando un report completo con il formato di output specificato, un riferimento alla fonte dati denominata e opzioni aggiuntive. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_11)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Popola il documento modello con dati provenienti da più fonti, generando un report completo con un formato di output specificato e opzioni aggiuntive. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Popola il documento modello con dati provenienti da più fonti. Esegue il rendering in immagini. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages_1)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Popola il documento modello con dati provenienti da più fonti. Esegue il rendering in immagini. |

### Guarda anche

* class [Processor](../processor/)
* spazio dei nomi [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../)
