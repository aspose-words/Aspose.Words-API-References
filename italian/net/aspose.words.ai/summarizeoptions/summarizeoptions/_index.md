---
title: SummarizeOptions
linktitle: SummarizeOptions
articleTitle: SummarizeOptions
second_title: Aspose.Words per .NET
description: Scopri il costruttore SummarizeOptions per creare istanze personalizzate della classe SummarizeOptions, migliorando l'efficienza e la flessibilità della tua codifica.
type: docs
weight: 10
url: /it/net/aspose.words.ai/summarizeoptions/summarizeoptions/
---
## SummarizeOptions constructor

Inizializza una nuova istanza di[`SummarizeOptions`](../) classe.

```csharp
public SummarizeOptions()
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

* class [SummarizeOptions](../)
* spazio dei nomi [Aspose.Words.AI](../../../aspose.words.ai/)
* assemblea [Aspose.Words](../../../)
