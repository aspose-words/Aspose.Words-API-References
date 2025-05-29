---
title: IAiModelText.Summarize
linktitle: Summarize
articleTitle: Summarize
second_title: Aspose.Words для .NET
description: Легко резюмируйте документы с помощью IAiModelText. Настройте длину резюмирования с помощью передового ИИ для точного извлечения контента и улучшения читаемости.
type: docs
weight: 20
url: /ru/net/aspose.words.ai/iaimodeltext/summarize/
---
## Summarize(*[Document](../../../aspose.words/document/), [SummarizeOptions](../../summarizeoptions/)*) {#summarize}

Создает резюме указанного документа с возможностью настройки длины резюме. Эта операция использует подключенную модель ИИ для обработки контента.

```csharp
public Document Summarize(Document sourceDocument, SummarizeOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceDocument | Document | Документ подлежит обобщению. |
| options | SummarizeOptions | Дополнительные настройки для управления длиной резюме и другими параметрами. |

### Возвращаемое значение

Краткая версия содержания документа.

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

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* пространство имен [Aspose.Words.AI](../../../aspose.words.ai/)
* сборка [Aspose.Words](../../../)

---

## Summarize(*Document[], [SummarizeOptions](../../summarizeoptions/)*) {#summarize_1}

Создает сводки для массива документов с возможностью управления длиной сводки и другими параметрами. Этот метод использует подключенную модель ИИ для обработки каждого документа в массиве.

```csharp
public Document Summarize(Document[] sourceDocuments, SummarizeOptions options = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceDocuments | Document[] | Массив документов, подлежащих обобщению. |
| options | SummarizeOptions | Дополнительные настройки для управления длиной резюме и другими параметрами |

### Возвращаемое значение

Краткая версия содержания документа.

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

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* пространство имен [Aspose.Words.AI](../../../aspose.words.ai/)
* сборка [Aspose.Words](../../../)
