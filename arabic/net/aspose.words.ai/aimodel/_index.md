---
title: AiModel Class
linktitle: AiModel
articleTitle: AiModel
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.AI.AiModel، وهي مفتاحك للاستفادة من نماذج اللغة التوليدية المتقدمة لتحسين توليد النصوص وأتمتتها.
type: docs
weight: 20
url: /ar/net/aspose.words.ai/aimodel/
---
## AiModel class

يمثل معلومات حول نموذج اللغة التوليدية.

```csharp
public abstract class AiModel
```

## طُرق

| اسم | وصف |
| --- | --- |
| static [Create](../../aspose.words.ai/aimodel/create/)(*[AiModelType](../aimodeltype/)*) | ينشئ مثيلًا جديدًا لـ`AiModel` الصف. |
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

* مساحة الاسم [Aspose.Words.AI](../../aspose.words.ai/)
* المجسم [Aspose.Words](../../)
