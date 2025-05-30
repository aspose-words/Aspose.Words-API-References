---
title: OpenAiModel Class
linktitle: OpenAiModel
articleTitle: OpenAiModel
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.AI.OpenAiModel la tua porta verso un'integrazione perfetta con i potenti modelli linguistici di OpenAI per un'elaborazione avanzata dei documenti.
type: docs
weight: 90
url: /it/net/aspose.words.ai/openaimodel/
---
## OpenAiModel class

Una classe astratta che rappresenta l'integrazione con i grandi modelli linguistici di OpenAI all'interno di Aspose.Words.

```csharp
public abstract class OpenAiModel : AiModel, IAiModelText
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Imposta una chiave API specificata sul modello. |
| [WithOrganization](../../aspose.words.ai/openaimodel/withorganization/)(*string*) | Imposta un'organizzazione specificata sul modello. |
| [WithProject](../../aspose.words.ai/openaimodel/withproject/)(*string*) | Imposta un progetto specificato sul modello. |

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

* class [AiModel](../aimodel/)
* interface [IAiModelText](../iaimodeltext/)
* spazio dei nomi [Aspose.Words.AI](../../aspose.words.ai/)
* assemblea [Aspose.Words](../../)
