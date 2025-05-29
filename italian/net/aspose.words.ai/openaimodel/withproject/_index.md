---
title: OpenAiModel.WithProject
linktitle: WithProject
articleTitle: WithProject
second_title: Aspose.Words per .NET
description: Migliora le tue capacità di intelligenza artificiale con il metodo WithProject di OpenAiModel: assegna facilmente progetti per ottimizzare le prestazioni e semplificare il flusso di lavoro.
type: docs
weight: 20
url: /it/net/aspose.words.ai/openaimodel/withproject/
---
## OpenAiModel.WithProject method

Imposta un progetto specificato sul modello.

```csharp
public OpenAiModel WithProject(string projectId)
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

* class [OpenAiModel](../)
* spazio dei nomi [Aspose.Words.AI](../../../aspose.words.ai/)
* assemblea [Aspose.Words](../../../)
