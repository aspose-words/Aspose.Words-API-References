---
title: AiModel Class
linktitle: AiModel
articleTitle: AiModel
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.AI.AiModel, la chiave per sfruttare modelli linguistici generativi avanzati per una generazione e un'automazione migliorate del testo.
type: docs
weight: 20
url: /it/net/aspose.words.ai/aimodel/
---
## AiModel class

Rappresenta informazioni su un modello linguistico generativo.

```csharp
public abstract class AiModel
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| static [Create](../../aspose.words.ai/aimodel/create/)(*[AiModelType](../aimodeltype/)*) | Crea una nuova istanza di`AiModel` classe. |
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

* spazio dei nomi [Aspose.Words.AI](../../aspose.words.ai/)
* assemblea [Aspose.Words](../../)
