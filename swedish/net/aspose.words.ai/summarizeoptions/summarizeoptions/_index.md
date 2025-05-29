---
title: SummarizeOptions
linktitle: SummarizeOptions
articleTitle: SummarizeOptions
second_title: Aspose.Words för .NET
description: Upptäck konstruktorn SummarizeOptions för att skapa anpassade instanser av SummarizeOptions-klassen, vilket förbättrar din kodningseffektivitet och flexibilitet.
type: docs
weight: 10
url: /sv/net/aspose.words.ai/summarizeoptions/summarizeoptions/
---
## SummarizeOptions constructor

Initierar en ny instans av[`SummarizeOptions`](../) klass.

```csharp
public SummarizeOptions()
```

## Exempel

Visar hur man sammanfattar text med hjälp av OpenAI och Google-modeller.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Använd OpenAI eller Googles generativa språkmodeller.
IAiModelText model = ((OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey)).WithOrganization("Organization").WithProject("Project");

SummarizeOptions options = new SummarizeOptions();

options.SummaryLength = SummaryLength.Short;
Document oneDocumentSummary = model.Summarize(firstDoc, options);
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

options.SummaryLength = SummaryLength.Long;
Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, options);
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### Se även

* class [SummarizeOptions](../)
* namnutrymme [Aspose.Words.AI](../../../aspose.words.ai/)
* hopsättning [Aspose.Words](../../../)
