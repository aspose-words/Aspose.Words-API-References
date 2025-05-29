---
title: GoogleAiModel Class
linktitle: GoogleAiModel
articleTitle: GoogleAiModel
second_title: Aspose.Words لـ .NET
description: استخدم قوة فئة Aspose.Words.AI.GoogleAiModel لدمج نماذج Google AI بسلاسة، مما يعزز قدرات معالجة المستندات لديك دون عناء.
type: docs
weight: 60
url: /ar/net/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class

فئة مجردة تمثل التكامل مع نماذج الذكاء الاصطناعي الخاصة بشركة Google ضمن Aspose.Words.

```csharp
public abstract class GoogleAiModel : AiModel, IAiModelText
```

## طُرق

| اسم | وصف |
| --- | --- |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | تعيين مفتاح API محدد للنموذج. |

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

* class [AiModel](../aimodel/)
* interface [IAiModelText](../iaimodeltext/)
* مساحة الاسم [Aspose.Words.AI](../../aspose.words.ai/)
* المجسم [Aspose.Words](../../)
