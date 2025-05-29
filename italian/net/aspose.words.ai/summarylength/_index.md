---
title: SummaryLength Enum
linktitle: SummaryLength
articleTitle: SummaryLength
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.AI.SummaryLength, che offre opzioni flessibili per la lunghezza del riepilogo, per una migliore sintesi dei documenti e una maggiore chiarezza dei contenuti.
type: docs
weight: 110
url: /it/net/aspose.words.ai/summarylength/
---
## SummaryLength enumeration

Enumera le possibili lunghezze del riepilogo.

```csharp
public enum SummaryLength
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| VeryShort | `0` | Prova a generare 1-2 frasi. |
| Short | `1` | Prova a generare 3-4 frasi. |
| Medium | `2` | Prova a generare 5-6 frasi. |
| Long | `3` | Prova a generare 7-10 frasi. |
| VeryLong | `4` | Prova a generare 11-20 frasi. |

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
