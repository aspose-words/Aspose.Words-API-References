---
title: OpenAiModel.WithProject
linktitle: WithProject
articleTitle: WithProject
second_title: Aspose.Words для .NET
description: Расширьте возможности своего ИИ с помощью метода WithProject от OpenAiModel — легко назначайте проекты для оптимизации производительности и оптимизации рабочего процесса.
type: docs
weight: 20
url: /ru/net/aspose.words.ai/openaimodel/withproject/
---
## OpenAiModel.WithProject method

Устанавливает указанный проект для модели.

```csharp
public OpenAiModel WithProject(string projectId)
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
