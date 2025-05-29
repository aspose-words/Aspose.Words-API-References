---
title: OpenAiModel Class
linktitle: OpenAiModel
articleTitle: OpenAiModel
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.AI.OpenAiModel—بوابتك إلى التكامل السلس مع نماذج اللغة القوية الخاصة بـ OpenAI لتحسين معالجة المستندات.
type: docs
weight: 90
url: /ar/net/aspose.words.ai/openaimodel/
---
## OpenAiModel class

فئة مجردة تمثل التكامل مع نماذج اللغة الكبيرة الخاصة بـ OpenAI داخل Aspose.Words.

```csharp
public abstract class OpenAiModel : AiModel, IAiModelText
```

## طُرق

| اسم | وصف |
| --- | --- |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | تعيين مفتاح API محدد للنموذج. |
| [WithOrganization](../../aspose.words.ai/openaimodel/withorganization/)(*string*) | تعيين منظمة محددة للنموذج. |
| [WithProject](../../aspose.words.ai/openaimodel/withproject/)(*string*) | تعيين مشروع محدد للنموذج. |

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
