---
title: IAiModelText Interface
linktitle: IAiModelText
articleTitle: IAiModelText
second_title: Aspose.Words per .NET
description: Sfrutta il tuo potenziale creativo con Aspose.Words.AI.IAiModelText, l'interfaccia versatile per modelli di intelligenza artificiale che generano senza sforzo contenuti di testo diversificati e di alta qualità.
type: docs
weight: 70
url: /it/net/aspose.words.ai/iaimodeltext/
---
## IAiModelText interface

L'interfaccia comune per i modelli di intelligenza artificiale progettati per generare una varietà di contenuti basati su testo.

```csharp
public interface IAiModelText
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [CheckGrammar](../../aspose.words.ai/iaimodeltext/checkgrammar/)(*[Document](../../aspose.words/document/), [CheckGrammarOptions](../checkgrammaroptions/)*) | Controlla la grammatica del documento fornito. Questa operazione sfrutta il modello di intelligenza artificiale connesso per controllare la grammatica del documento. |
| [Summarize](../../aspose.words.ai/iaimodeltext/summarize/#summarize)(*[Document](../../aspose.words/document/), [SummarizeOptions](../summarizeoptions/)*) | Genera un riepilogo del documento specificato, con opzioni per regolare la lunghezza del riepilogo. Questa operazione sfrutta il modello di intelligenza artificiale connesso per l'elaborazione dei contenuti. |
| [Summarize](../../aspose.words.ai/iaimodeltext/summarize/#summarize_1)(*Document[], [SummarizeOptions](../summarizeoptions/)*) | Genera riepiloghi per una matrice di documenti, con opzioni per controllare la lunghezza del riepilogo e altre impostazioni. Questo metodo utilizza il modello di intelligenza artificiale connessa per elaborare ciascun documento nella matrice. |
| [Translate](../../aspose.words.ai/iaimodeltext/translate/)(*[Document](../../aspose.words/document/), [Language](../language/)*) | Traduce il documento fornito nella lingua di destinazione specificata. Questa operazione sfrutta il modello di intelligenza artificiale connesso per la traduzione dei contenuti. |

## Esempi

Mostra come riassumere il testo utilizzando i modelli OpenAI e Google.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Utilizza modelli linguistici generativi OpenAI o Google.
IAiModelText model = ((OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey)).WithOrganization("Organization").WithProject("Project");

SummarizeOptions options = new SummarizeOptions();

options.SummaryLength = SummaryLength.Short;
Document oneDocumentSummary = model.Summarize(firstDoc, options);
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

options.SummaryLength = SummaryLength.Long;
Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, options);
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.AI](../../aspose.words.ai/)
* assemblea [Aspose.Words](../../)
