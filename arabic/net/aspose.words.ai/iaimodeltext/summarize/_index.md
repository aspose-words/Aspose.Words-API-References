---
title: IAiModelText.Summarize
linktitle: Summarize
articleTitle: Summarize
second_title: Aspose.Words لـ .NET
description: لخّص مستنداتك بسهولة مع IAiModelText. خصّص طول الملخص باستخدام الذكاء الاصطناعي المتطور لاستخراج محتوى دقيق وتحسين قابلية القراءة.
type: docs
weight: 20
url: /ar/net/aspose.words.ai/iaimodeltext/summarize/
---
## Summarize(*[Document](../../../aspose.words/document/), [SummarizeOptions](../../summarizeoptions/)*) {#summarize}

يُنشئ ملخصًا للمستند المحدد، مع خيارات لضبط طول الملخص. تستفيد هذه العملية من نموذج الذكاء الاصطناعي المتصل لمعالجة المحتوى.

```csharp
public Document Summarize(Document sourceDocument, SummarizeOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| sourceDocument | Document | الوثيقة التي سيتم تلخيصها. |
| options | SummarizeOptions | إعدادات اختيارية للتحكم في طول الملخص والمعلمات الأخرى. |

### قيمة الإرجاع

نسخة مختصرة لمحتوى الوثيقة.

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

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* مساحة الاسم [Aspose.Words.AI](../../../aspose.words.ai/)
* المجسم [Aspose.Words](../../../)

---

## Summarize(*Document[], [SummarizeOptions](../../summarizeoptions/)*) {#summarize_1}

ينشئ ملخصات لمجموعة من المستندات، مع خيارات للتحكم في طول الملخص والإعدادات الأخرى. تستخدم هذه الطريقة نموذج الذكاء الاصطناعي المتصل لمعالجة كل مستند في المجموعة.

```csharp
public Document Summarize(Document[] sourceDocuments, SummarizeOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| sourceDocuments | Document[] | مجموعة من الوثائق التي سيتم تلخيصها. |
| options | SummarizeOptions | إعدادات اختيارية للتحكم في طول الملخص والمعلمات الأخرى |

### قيمة الإرجاع

نسخة مختصرة لمحتوى الوثيقة.

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

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* مساحة الاسم [Aspose.Words.AI](../../../aspose.words.ai/)
* المجسم [Aspose.Words](../../../)
