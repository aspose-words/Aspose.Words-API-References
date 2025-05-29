---
title: OpenAiModel.WithOrganization
linktitle: WithOrganization
articleTitle: WithOrganization
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل طريقة OpenAiModel WithOrganization على تعزيز تجربة الذكاء الاصطناعي لديك من خلال إعداد مؤسستك بسهولة لتحقيق الأداء الأمثل.
type: docs
weight: 10
url: /ar/net/aspose.words.ai/openaimodel/withorganization/
---
## OpenAiModel.WithOrganization method

تعيين منظمة محددة للنموذج.

```csharp
public OpenAiModel WithOrganization(string organizationId)
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

* class [OpenAiModel](../)
* مساحة الاسم [Aspose.Words.AI](../../../aspose.words.ai/)
* المجسم [Aspose.Words](../../../)
