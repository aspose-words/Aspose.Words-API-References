---
title: AiModel.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة AiModel Create لإنشاء مثيلات فئة AiModel جديدة بسهولة، مما يعزز تطوير الذكاء الاصطناعي لديك بكفاءة مبسطة.
type: docs
weight: 10
url: /ar/net/aspose.words.ai/aimodel/create/
---
## AiModel.Create method

ينشئ مثيلًا جديدًا لـ[`AiModel`](../) الصف.

```csharp
public static AiModel Create(AiModelType modelType)
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

* enum [AiModelType](../../aimodeltype/)
* class [AiModel](../)
* مساحة الاسم [Aspose.Words.AI](../../../aspose.words.ai/)
* المجسم [Aspose.Words](../../../)
