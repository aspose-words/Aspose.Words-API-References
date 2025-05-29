---
title: SummarizeOptions Class
linktitle: SummarizeOptions
articleTitle: SummarizeOptions
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.AI.SummarizeOptions per personalizzare e migliorare la sintesi dei tuoi documenti, per ottenere informazioni più chiare e una migliore gestione dei contenuti.
type: docs
weight: 100
url: /it/net/aspose.words.ai/summarizeoptions/
---
## SummarizeOptions class

Consente di specificare diverse opzioni per riassumere il contenuto del documento.

```csharp
public class SummarizeOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [SummarizeOptions](summarizeoptions/)() | Inizializza una nuova istanza di`SummarizeOptions` classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [SummaryLength](../../aspose.words.ai/summarizeoptions/summarylength/) { get; set; } | Consente di specificare la lunghezza del riepilogo. Il valore predefinito èMedium . |

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
