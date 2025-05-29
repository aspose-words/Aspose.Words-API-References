---
title: SummarizeOptions Class
linktitle: SummarizeOptions
articleTitle: SummarizeOptions
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.AI.SummarizeOptions لتخصيص وتحسين تلخيص مستنداتك للحصول على رؤى أكثر وضوحًا وإدارة محتوى محسّنة.
type: docs
weight: 100
url: /ar/net/aspose.words.ai/summarizeoptions/
---
## SummarizeOptions class

يسمح بتحديد خيارات مختلفة لتلخيص محتوى المستند.

```csharp
public class SummarizeOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [SummarizeOptions](summarizeoptions/)() | يقوم بتهيئة مثيلات جديدة من`SummarizeOptions` الصف. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [SummaryLength](../../aspose.words.ai/summarizeoptions/summarylength/) { get; set; } | يسمح بتحديد طول الملخص. القيمة الافتراضية هيMedium . |

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
