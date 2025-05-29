---
title: SummarizeOptions.SummaryLength
linktitle: SummaryLength
articleTitle: SummaryLength
second_title: Aspose.Words для .NET
description: Управляйте длиной резюме с помощью свойства SummarizeOptions SummaryLength. Настройте содержимое для ясности и воздействия. По умолчанию — Medium.
type: docs
weight: 20
url: /ru/net/aspose.words.ai/summarizeoptions/summarylength/
---
## SummarizeOptions.SummaryLength property

Позволяет указать длину резюме. Значение по умолчанию:Medium .

```csharp
public SummaryLength SummaryLength { get; set; }
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

* enum [SummaryLength](../../summarylength/)
* class [SummarizeOptions](../)
* пространство имен [Aspose.Words.AI](../../../aspose.words.ai/)
* сборка [Aspose.Words](../../../)
