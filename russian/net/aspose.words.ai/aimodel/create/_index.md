---
title: AiModel.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words для .NET
description: Откройте для себя метод AiModel Create, позволяющий легко создавать новые экземпляры класса AiModel, что позволит оптимизировать и оптимизировать разработку ИИ.
type: docs
weight: 10
url: /ru/net/aspose.words.ai/aimodel/create/
---
## AiModel.Create method

Создает новый экземпляр[`AiModel`](../) класс.

```csharp
public static AiModel Create(AiModelType modelType)
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

* enum [AiModelType](../../aimodeltype/)
* class [AiModel](../)
* пространство имен [Aspose.Words.AI](../../../aspose.words.ai/)
* сборка [Aspose.Words](../../../)
