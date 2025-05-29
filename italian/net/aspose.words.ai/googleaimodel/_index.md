---
title: GoogleAiModel Class
linktitle: GoogleAiModel
articleTitle: GoogleAiModel
second_title: Aspose.Words per .NET
description: Sfrutta la potenza della classe Aspose.Words.AI.GoogleAiModel per integrare perfettamente i modelli di Google AI, migliorando senza sforzo le tue capacità di elaborazione dei documenti.
type: docs
weight: 60
url: /it/net/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class

Una classe astratta che rappresenta l'integrazione con i modelli di intelligenza artificiale di Google all'interno di Aspose.Words.

```csharp
public abstract class GoogleAiModel : AiModel, IAiModelText
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Imposta una chiave API specificata sul modello. |

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
