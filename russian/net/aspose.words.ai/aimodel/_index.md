---
title: AiModel Class
linktitle: AiModel
articleTitle: AiModel
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.AI.AiModel — ваш ключ к использованию расширенных моделей генеративного языка для улучшенной генерации текста и автоматизации.
type: docs
weight: 20
url: /ru/net/aspose.words.ai/aimodel/
---
## AiModel class

Представляет информацию о генеративной языковой модели.

```csharp
public abstract class AiModel
```

## Методы

| Имя | Описание |
| --- | --- |
| static [Create](../../aspose.words.ai/aimodel/create/)(*[AiModelType](../aimodeltype/)*) | Создает новый экземпляр`AiModel` класс. |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Устанавливает указанный ключ API для модели. |

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
