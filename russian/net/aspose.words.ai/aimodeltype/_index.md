---
title: AiModelType Enum
linktitle: AiModelType
articleTitle: AiModelType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.AI.AiModelType для бесшовной интеграции моделей ИИ в обработку документов, повышения эффективности и производительности.
type: docs
weight: 30
url: /ru/net/aspose.words.ai/aimodeltype/
---
## AiModelType enumeration

Представляет типы[`AiModel`](../aimodel/) которые можно интегрировать в рабочий процесс обработки документов.

```csharp
public enum AiModelType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Gpt4O | `0` | Тип генеративной модели GPT-4o. |
| Gpt4OMini | `1` | Тип генеративной модели GPT-4o mini. |
| Gpt4Turbo | `2` | Тип генеративной модели GPT-4 Turbo. |
| Gpt35Turbo | `3` | Тип генеративной модели GPT-3.5 Turbo. |
| Gemini15Flash | `4` | Тип генеративной модели Gemini 1.5 Flash. |
| Gemini15Flash8B | `5` | Тип генеративной модели Gemini 1.5 Flash-8B. |
| Gemini15Pro | `6` | Тип генеративной модели Gemini 1.5 Pro. |
| Claude35Sonnet | `7` | Клод 3.5 Сонет генеративная модель тип. |
| Claude35Haiku | `8` | Тип генеративной модели Клода 3.5 Хайку. |
| Claude3Opus | `9` | Тип генеративной модели Клода 3 Опуса. |
| Claude3Sonnet | `10` | Тип генеративной модели Клода 3 Сонета. |
| Claude3Haiku | `11` | Тип генеративной модели Клода 3 Хайку. |

## Примечания

Это перечисление используется для определения того, какую большую языковую модель (LLM) следует использовать для задач , таких как реферирование, перевод и генерация контента.

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
