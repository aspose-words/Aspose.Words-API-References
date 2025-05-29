---
title: AiModel.WithApiKey
linktitle: WithApiKey
articleTitle: WithApiKey
second_title: Aspose.Words لـ .NET
description: استغل قوة AiModel باستخدام طريقة WithApiKey. عيّن مفتاح API الخاص بك بسهولة لتحسين الأداء والتكامل بسلاسة.
type: docs
weight: 20
url: /ar/net/aspose.words.ai/aimodel/withapikey/
---
## AiModel.WithApiKey method

تعيين مفتاح API محدد للنموذج.

```csharp
public AiModel WithApiKey(string apiKey)
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

* class [AiModel](../)
* مساحة الاسم [Aspose.Words.AI](../../../aspose.words.ai/)
* المجسم [Aspose.Words](../../../)
