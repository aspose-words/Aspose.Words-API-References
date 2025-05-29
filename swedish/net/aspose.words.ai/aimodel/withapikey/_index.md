---
title: AiModel.WithApiKey
linktitle: WithApiKey
articleTitle: WithApiKey
second_title: Aspose.Words för .NET
description: Lås upp kraften i AiModel med WithApiKey-metoden. Ställ enkelt in din API-nyckel för förbättrad funktionalitet och sömlös integration.
type: docs
weight: 20
url: /sv/net/aspose.words.ai/aimodel/withapikey/
---
## AiModel.WithApiKey method

Ställer in en specificerad API-nyckel för modellen.

```csharp
public AiModel WithApiKey(string apiKey)
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

* class [AiModel](../)
* namnutrymme [Aspose.Words.AI](../../../aspose.words.ai/)
* hopsättning [Aspose.Words](../../../)
