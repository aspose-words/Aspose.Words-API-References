---
title: AiModel.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words för .NET
description: Upptäck AiModel Create-metoden för att enkelt generera nya AiModel-klassinstanser och förbättra din AI-utveckling med strömlinjeformad effektivitet.
type: docs
weight: 10
url: /sv/net/aspose.words.ai/aimodel/create/
---
## AiModel.Create method

Skapar en ny instans av[`AiModel`](../) klass.

```csharp
public static AiModel Create(AiModelType modelType)
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

* enum [AiModelType](../../aimodeltype/)
* class [AiModel](../)
* namnutrymme [Aspose.Words.AI](../../../aspose.words.ai/)
* hopsättning [Aspose.Words](../../../)
