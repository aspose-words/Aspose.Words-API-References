---
title: SummaryLength Enum
linktitle: SummaryLength
articleTitle: SummaryLength
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.AI.SummaryLength، التي توفر خيارات مرنة لطول الملخص لتحسين تلخيص المستندات وتحسين وضوح المحتوى.
type: docs
weight: 110
url: /ar/net/aspose.words.ai/summarylength/
---
## SummaryLength enumeration

يقوم بإحصاء أطوال الملخص المحتملة.

```csharp
public enum SummaryLength
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| VeryShort | `0` | حاول إنشاء 1-2 جملة. |
| Short | `1` | حاول إنشاء 3-4 جمل. |
| Medium | `2` | حاول إنشاء 5-6 جمل. |
| Long | `3` | حاول إنشاء 7-10 جمل. |
| VeryLong | `4` | حاول إنشاء 11-20 جملة. |

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
