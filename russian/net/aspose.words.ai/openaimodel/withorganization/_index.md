---
title: OpenAiModel.WithOrganization
linktitle: WithOrganization
articleTitle: WithOrganization
second_title: Aspose.Words для .NET
description: Узнайте, как метод OpenAiModel WithOrganization расширяет возможности вашего ИИ, легко настраивая вашу организацию на оптимальную производительность.
type: docs
weight: 10
url: /ru/net/aspose.words.ai/openaimodel/withorganization/
---
## OpenAiModel.WithOrganization method

Устанавливает указанную организацию для модели.

```csharp
public OpenAiModel WithOrganization(string organizationId)
```

## Примеры

Показывает, как резюмировать текст с использованием моделей OpenAI и Google.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Используйте модели генеративного языка OpenAI или Google.
IAiModelText model = ((OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey)).WithOrganization("Organization").WithProject("Project");

SummarizeOptions options = new SummarizeOptions();

options.SummaryLength = SummaryLength.Short;
Document oneDocumentSummary = model.Summarize(firstDoc, options);
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

options.SummaryLength = SummaryLength.Long;
Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, options);
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### Смотрите также

* class [OpenAiModel](../)
* пространство имен [Aspose.Words.AI](../../../aspose.words.ai/)
* сборка [Aspose.Words](../../../)
