---
title: SummaryLength Enum
linktitle: SummaryLength
articleTitle: SummaryLength
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.AI.SummaryLength, предлагающее гибкие параметры длины резюме для улучшенного реферирования документов и повышения ясности содержания.
type: docs
weight: 110
url: /ru/net/aspose.words.ai/summarylength/
---
## SummaryLength enumeration

Перечисляет возможные длины резюме.

```csharp
public enum SummaryLength
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| VeryShort | `0` | Попробуйте составить 1-2 предложения. |
| Short | `1` | Попробуйте составить 3-4 предложения. |
| Medium | `2` | Попробуйте составить 5-6 предложений. |
| Long | `3` | Попробуйте составить 7-10 предложений. |
| VeryLong | `4` | Попробуйте составить 11-20 предложений. |

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
