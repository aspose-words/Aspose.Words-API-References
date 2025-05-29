---
title: IAiModelText Interface
linktitle: IAiModelText
articleTitle: IAiModelText
second_title: Aspose.Words لـ .NET
description: أطلق العنان لإمكانياتك الإبداعية باستخدام Aspose.Words.AI.IAiModelText، وهي الواجهة متعددة الاستخدامات لنماذج الذكاء الاصطناعي التي تولد محتوى نصيًا متنوعًا وعالي الجودة بكل سهولة.
type: docs
weight: 70
url: /ar/net/aspose.words.ai/iaimodeltext/
---
## IAiModelText interface

الواجهة المشتركة لنماذج الذكاء الاصطناعي المصممة لتوليد مجموعة متنوعة من المحتوى النصي.

```csharp
public interface IAiModelText
```

## طُرق

| اسم | وصف |
| --- | --- |
| [CheckGrammar](../../aspose.words.ai/iaimodeltext/checkgrammar/)(*[Document](../../aspose.words/document/), [CheckGrammarOptions](../checkgrammaroptions/)*) | يتحقق من قواعد اللغة للمستند المقدم. تستفيد هذه العملية من نموذج الذكاء الاصطناعي المتصل للتحقق من قواعد اللغة للمستند. |
| [Summarize](../../aspose.words.ai/iaimodeltext/summarize/#summarize)(*[Document](../../aspose.words/document/), [SummarizeOptions](../summarizeoptions/)*) | يُنشئ ملخصًا للمستند المحدد، مع خيارات لضبط طول الملخص. تستفيد هذه العملية من نموذج الذكاء الاصطناعي المتصل لمعالجة المحتوى. |
| [Summarize](../../aspose.words.ai/iaimodeltext/summarize/#summarize_1)(*Document[], [SummarizeOptions](../summarizeoptions/)*) | ينشئ ملخصات لمجموعة من المستندات، مع خيارات للتحكم في طول الملخص والإعدادات الأخرى. تستخدم هذه الطريقة نموذج الذكاء الاصطناعي المتصل لمعالجة كل مستند في المجموعة. |
| [Translate](../../aspose.words.ai/iaimodeltext/translate/)(*[Document](../../aspose.words/document/), [Language](../language/)*) | يترجم المستند المقدم إلى لغة الهدف المحددة. تستفيد هذه العملية من نموذج الذكاء الاصطناعي المتصل لترجمة المحتوى. |

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
