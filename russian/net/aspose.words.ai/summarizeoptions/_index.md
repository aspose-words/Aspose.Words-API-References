---
title: SummarizeOptions Class
linktitle: SummarizeOptions
articleTitle: SummarizeOptions
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.AI.SummarizeOptions, чтобы настроить и улучшить реферирование документов для получения более четких сведений и улучшенного управления контентом.
type: docs
weight: 100
url: /ru/net/aspose.words.ai/summarizeoptions/
---
## SummarizeOptions class

Позволяет указать различные параметры для резюмирования содержимого документа.

```csharp
public class SummarizeOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [SummarizeOptions](summarizeoptions/)() | Инициализирует новые экземпляры`SummarizeOptions` класс. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [SummaryLength](../../aspose.words.ai/summarizeoptions/summarylength/) { get; set; } | Позволяет указать длину резюме. Значение по умолчанию:Medium . |

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

* пространство имен [Aspose.Words.AI](../../aspose.words.ai/)
* сборка [Aspose.Words](../../)
