---
title: AiModelType Enum
linktitle: AiModelType
articleTitle: AiModelType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.AI.AiModelType enum للتكامل السلس لنماذج الذكاء الاصطناعي في معالجة المستندات، مما يعزز الكفاءة والإنتاجية.
type: docs
weight: 30
url: /ar/net/aspose.words.ai/aimodeltype/
---
## AiModelType enumeration

يمثل أنواع[`AiModel`](../aimodel/) والتي يمكن دمجها في سير عمل معالجة المستندات.

```csharp
public enum AiModelType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Gpt4O | `0` | نوع النموذج التوليدي GPT-4o. |
| Gpt4OMini | `1` | نوع النموذج التوليدي الصغير GPT-4o. |
| Gpt4Turbo | `2` | نوع النموذج التوليدي GPT-4 Turbo. |
| Gpt35Turbo | `3` | نوع النموذج التوليدي GPT-3.5 Turbo. |
| Gemini15Flash | `4` | نوع النموذج التوليدي لـ Gemini 1.5 Flash. |
| Gemini15Flash8B | `5` | نوع النموذج التوليدي Gemini 1.5 Flash-8B. |
| Gemini15Pro | `6` | نوع النموذج التوليدي لـ Gemini 1.5 Pro. |
| Claude35Sonnet | `7` | نوع النموذج التوليدي للسوناتة Claude 3.5. |
| Claude35Haiku | `8` | نوع النموذج التوليدي Claude 3.5 Haiku. |
| Claude3Opus | `9` | نوع النموذج التوليدي Claude 3 Opus. |
| Claude3Sonnet | `10` | نوع النموذج التوليدي لسوناتة كلود 3. |
| Claude3Haiku | `11` | نوع النموذج التوليدي Claude 3 Haiku. |

## ملاحظات

يستخدم هذا التعداد لتحديد نموذج اللغة الكبير (LLM) الذي يجب استخدامه للمهام مثل التلخيص والترجمة وتوليد المحتوى.

## أمثلة

يوضح كيفية تلخيص النص باستخدام نماذج OpenAI وGoogle.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// استخدم نماذج اللغة التوليدية OpenAI أو Google.
IAiModelText model = ((OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey)).WithOrganization("Organization").WithProject("Project");

SummarizeOptions options = new SummarizeOptions();

options.SummaryLength = SummaryLength.Short;
Document oneDocumentSummary = model.Summarize(firstDoc, options);
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

options.SummaryLength = SummaryLength.Long;
Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, options);
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.AI](../../aspose.words.ai/)
* المجسم [Aspose.Words](../../)
