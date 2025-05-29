---
title: AiModelType Enum
linktitle: AiModelType
articleTitle: AiModelType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.AI.AiModelType per un'integrazione perfetta dei modelli di intelligenza artificiale nell'elaborazione dei documenti, migliorando l'efficienza e la produttività.
type: docs
weight: 30
url: /it/net/aspose.words.ai/aimodeltype/
---
## AiModelType enumeration

Rappresenta i tipi di[`AiModel`](../aimodel/) che può essere integrato nel flusso di lavoro di elaborazione dei documenti.

```csharp
public enum AiModelType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Gpt4O | `0` | Tipo di modello generativo GPT-4o. |
| Gpt4OMini | `1` | Tipo di modello generativo mini GPT-4o. |
| Gpt4Turbo | `2` | Tipo di modello generativo GPT-4 Turbo. |
| Gpt35Turbo | `3` | Tipo di modello generativo GPT-3.5 Turbo. |
| Gemini15Flash | `4` | Tipo di modello generativo Flash Gemini 1.5. |
| Gemini15Flash8B | `5` | Tipo di modello generativo Flash-8B Gemini 1.5. |
| Gemini15Pro | `6` | Tipo di modello generativo Gemini 1.5 Pro. |
| Claude35Sonnet | `7` | Tipo di modello generativo Claude 3.5 Sonnet. |
| Claude35Haiku | `8` | Tipo di modello generativo Haiku di Claude 3.5. |
| Claude3Opus | `9` | Tipo di modello generativo Claude 3 Opus. |
| Claude3Sonnet | `10` | Tipo di modello generativo del sonetto Claude 3. |
| Claude3Haiku | `11` | Tipo di modello generativo Haiku di Claude 3. |

## Osservazioni

Questa enumerazione viene utilizzata per definire quale modello linguistico di grandi dimensioni (LLM) deve essere utilizzato per attività quali riepilogo, traduzione e generazione di contenuti.

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
