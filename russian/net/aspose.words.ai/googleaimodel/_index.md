---
title: GoogleAiModel Class
linktitle: GoogleAiModel
articleTitle: GoogleAiModel
second_title: Aspose.Words для .NET
description: Откройте для себя возможности класса Aspose.Words.AI.GoogleAiModel для бесшовной интеграции моделей Google AI, что позволит вам без труда расширить возможности обработки документов.
type: docs
weight: 60
url: /ru/net/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class

Абстрактный класс, представляющий интеграцию с моделями ИИ Google в Aspose.Words.

```csharp
public abstract class GoogleAiModel : AiModel, IAiModelText
```

## Методы

| Имя | Описание |
| --- | --- |
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

* class [AiModel](../aimodel/)
* interface [IAiModelText](../iaimodeltext/)
* пространство имен [Aspose.Words.AI](../../aspose.words.ai/)
* сборка [Aspose.Words](../../)
