---
title: SummarizeOptions.SummaryLength
linktitle: SummaryLength
articleTitle: SummaryLength
second_title: Aspose.Words لـ .NET
description: تحكم في طول ملخصك باستخدام خاصية SummarizeOptions SummaryLength. خصّص محتواك لزيادة الوضوح والتأثير. الإعداد الافتراضي هو متوسط.
type: docs
weight: 20
url: /ar/net/aspose.words.ai/summarizeoptions/summarylength/
---
## SummarizeOptions.SummaryLength property

يسمح بتحديد طول الملخص. القيمة الافتراضية هيMedium .

```csharp
public SummaryLength SummaryLength { get; set; }
```

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

* enum [SummaryLength](../../summarylength/)
* class [SummarizeOptions](../)
* مساحة الاسم [Aspose.Words.AI](../../../aspose.words.ai/)
* المجسم [Aspose.Words](../../../)
