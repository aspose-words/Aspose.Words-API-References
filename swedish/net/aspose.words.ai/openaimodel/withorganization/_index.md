---
title: OpenAiModel.WithOrganization
linktitle: WithOrganization
articleTitle: WithOrganization
second_title: Aspose.Words för .NET
description: Upptäck hur OpenAiModel WithOrganization-metoden förbättrar din AI-upplevelse genom att enkelt ställa in din organisation för optimerad prestanda.
type: docs
weight: 10
url: /sv/net/aspose.words.ai/openaimodel/withorganization/
---
## OpenAiModel.WithOrganization method

Ställer in en specificerad organisation för modellen.

```csharp
public OpenAiModel WithOrganization(string organizationId)
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

* class [OpenAiModel](../)
* namnutrymme [Aspose.Words.AI](../../../aspose.words.ai/)
* hopsättning [Aspose.Words](../../../)
