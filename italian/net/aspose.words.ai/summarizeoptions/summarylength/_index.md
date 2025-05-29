---
title: SummarizeOptions.SummaryLength
linktitle: SummaryLength
articleTitle: SummaryLength
second_title: Aspose.Words per .NET
description: Controlla la lunghezza del riepilogo con la proprietà SummaryLength di SummarizeOptions. Personalizza il contenuto per maggiore chiarezza e impatto. L'impostazione predefinita è Media.
type: docs
weight: 20
url: /it/net/aspose.words.ai/summarizeoptions/summarylength/
---
## SummarizeOptions.SummaryLength property

Consente di specificare la lunghezza del riepilogo. Il valore predefinito èMedium .

```csharp
public SummaryLength SummaryLength { get; set; }
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

* enum [SummaryLength](../../summarylength/)
* class [SummarizeOptions](../)
* spazio dei nomi [Aspose.Words.AI](../../../aspose.words.ai/)
* assemblea [Aspose.Words](../../../)
