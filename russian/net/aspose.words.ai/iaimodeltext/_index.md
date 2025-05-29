---
title: IAiModelText Interface
linktitle: IAiModelText
articleTitle: IAiModelText
second_title: Aspose.Words для .NET
description: Раскройте творческий потенциал с помощью Aspose.Words.AI.IAiModelText — универсального интерфейса для моделей ИИ, которые с легкостью генерируют разнообразный высококачественный текстовый контент.
type: docs
weight: 70
url: /ru/net/aspose.words.ai/iaimodeltext/
---
## IAiModelText interface

Общий интерфейс для моделей ИИ, предназначенный для генерации разнообразного текстового контента.

```csharp
public interface IAiModelText
```

## Методы

| Имя | Описание |
| --- | --- |
| [CheckGrammar](../../aspose.words.ai/iaimodeltext/checkgrammar/)(*[Document](../../aspose.words/document/), [CheckGrammarOptions](../checkgrammaroptions/)*) | Проверяет грамматику предоставленного документа. Эта операция использует подключенную модель ИИ для проверки грамматики документа. |
| [Summarize](../../aspose.words.ai/iaimodeltext/summarize/#summarize)(*[Document](../../aspose.words/document/), [SummarizeOptions](../summarizeoptions/)*) | Создает резюме указанного документа с возможностью настройки длины резюме. Эта операция использует подключенную модель ИИ для обработки контента. |
| [Summarize](../../aspose.words.ai/iaimodeltext/summarize/#summarize_1)(*Document[], [SummarizeOptions](../summarizeoptions/)*) | Создает сводки для массива документов с возможностью управления длиной сводки и другими параметрами. Этот метод использует подключенную модель ИИ для обработки каждого документа в массиве. |
| [Translate](../../aspose.words.ai/iaimodeltext/translate/)(*[Document](../../aspose.words/document/), [Language](../language/)*) | Переводит предоставленный документ на указанный целевой язык. Эта операция использует подключенную модель ИИ для перевода контента. |

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
