---
title: AiModel.WithApiKey
linktitle: WithApiKey
articleTitle: WithApiKey
second_title: Aspose.Words per .NET
description: Sfrutta la potenza di AiModel con il metodo WithApiKey. Imposta facilmente la tua chiave API per funzionalità avanzate e un'integrazione perfetta.
type: docs
weight: 20
url: /it/net/aspose.words.ai/aimodel/withapikey/
---
## AiModel.WithApiKey method

Imposta una chiave API specificata sul modello.

```csharp
public AiModel WithApiKey(string apiKey)
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

* class [AiModel](../)
* spazio dei nomi [Aspose.Words.AI](../../../aspose.words.ai/)
* assemblea [Aspose.Words](../../../)
