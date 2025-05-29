---
title: OpenAiModel Class
linktitle: OpenAiModel
articleTitle: OpenAiModel
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.AI.OpenAiModel — ваш шлюз к бесшовной интеграции с мощными языковыми моделями OpenAI для улучшенной обработки документов.
type: docs
weight: 90
url: /ru/net/aspose.words.ai/openaimodel/
---
## OpenAiModel class

Абстрактный класс, представляющий интеграцию с большими языковыми моделями OpenAI в Aspose.Words.

```csharp
public abstract class OpenAiModel : AiModel, IAiModelText
```

## Методы

| Имя | Описание |
| --- | --- |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Устанавливает указанный ключ API для модели. |
| [WithOrganization](../../aspose.words.ai/openaimodel/withorganization/)(*string*) | Устанавливает указанную организацию для модели. |
| [WithProject](../../aspose.words.ai/openaimodel/withproject/)(*string*) | Устанавливает указанный проект для модели. |

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
