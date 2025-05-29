---
title: AiModel.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words per .NET
description: Scopri il metodo AiModel Create per generare senza sforzo nuove istanze della classe AiModel, migliorando lo sviluppo dell'intelligenza artificiale con efficienza ottimizzata.
type: docs
weight: 10
url: /it/net/aspose.words.ai/aimodel/create/
---
## AiModel.Create method

Crea una nuova istanza di[`AiModel`](../) classe.

```csharp
public static AiModel Create(AiModelType modelType)
```

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

* enum [AiModelType](../../aimodeltype/)
* class [AiModel](../)
* spazio dei nomi [Aspose.Words.AI](../../../aspose.words.ai/)
* assemblea [Aspose.Words](../../../)
