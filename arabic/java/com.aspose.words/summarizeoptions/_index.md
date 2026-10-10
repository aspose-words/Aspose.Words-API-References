---
title: "SummarizeOptions"
linktitle: "SummarizeOptions"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد خيارات مختلفة لتلخيص محتوى المستند في Java."
type: docs
weight: 646
url: /ar/java/com.aspose.words/summarizeoptions/
---

**Inheritance:**
java.lang.Object
```
public class SummarizeOptions
```

يسمح بتحديد خيارات مختلفة لتلخيص محتوى المستند.

 **Examples:** 

يظهر كيفية تلخيص النص باستخدام نماذج OpenAI وGoogle.

```

 Document firstDoc = new Document(getMyDir() + "Big document.docx");
 Document secondDoc = new Document(getMyDir() + "Document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use OpenAI or Google generative language models.
 AiModel model = ((OpenAiModel)AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey)).withOrganization("Organization").withProject("Project");

 SummarizeOptions options = new SummarizeOptions();

 options.setSummaryLength(SummaryLength.SHORT);
 Document oneDocumentSummary = model.summarize(firstDoc, options);
 oneDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.One.docx");

 options.setSummaryLength(SummaryLength.LONG);
 Document multiDocumentSummary = model.summarize(new Document[] { firstDoc, secondDoc }, options);
 multiDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.Multi.docx");
 
```
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [SummarizeOptions()](#SummarizeOptions) | ينشئ مثلاً جديداً من الفئة [SummarizeOptions](../../com.aspose.words/summarizeoptions/). |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getSummaryLength()](#getSummaryLength) | يسمح بتحديد طول الملخص. |
| [setSummaryLength(int value)](#setSummaryLength-int) | يسمح بتحديد طول الملخص. |
### SummarizeOptions() {#SummarizeOptions}
```
public SummarizeOptions()
```


ينشئ مثلاً جديداً من الفئة [SummarizeOptions](../../com.aspose.words/summarizeoptions/).

 **Examples:** 

يظهر كيفية تلخيص النص باستخدام نماذج OpenAI وGoogle.

```

 Document firstDoc = new Document(getMyDir() + "Big document.docx");
 Document secondDoc = new Document(getMyDir() + "Document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use OpenAI or Google generative language models.
 AiModel model = ((OpenAiModel)AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey)).withOrganization("Organization").withProject("Project");

 SummarizeOptions options = new SummarizeOptions();

 options.setSummaryLength(SummaryLength.SHORT);
 Document oneDocumentSummary = model.summarize(firstDoc, options);
 oneDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.One.docx");

 options.setSummaryLength(SummaryLength.LONG);
 Document multiDocumentSummary = model.summarize(new Document[] { firstDoc, secondDoc }, options);
 multiDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.Multi.docx");
 
```

### getSummaryLength() {#getSummaryLength}
```
public int getSummaryLength()
```


يسمح بتحديد طول الملخص. القيمة الافتراضية هي [SummaryLength.MEDIUM](../../com.aspose.words/summarylength/\#MEDIUM).

 **Examples:** 

يظهر كيفية تلخيص النص باستخدام نماذج OpenAI وGoogle.

```

 Document firstDoc = new Document(getMyDir() + "Big document.docx");
 Document secondDoc = new Document(getMyDir() + "Document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use OpenAI or Google generative language models.
 AiModel model = ((OpenAiModel)AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey)).withOrganization("Organization").withProject("Project");

 SummarizeOptions options = new SummarizeOptions();

 options.setSummaryLength(SummaryLength.SHORT);
 Document oneDocumentSummary = model.summarize(firstDoc, options);
 oneDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.One.docx");

 options.setSummaryLength(SummaryLength.LONG);
 Document multiDocumentSummary = model.summarize(new Document[] { firstDoc, secondDoc }, options);
 multiDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.Multi.docx");
 
```

**Returns:**
int - القيمة int المقابلة. القيمة المرجعة هي واحدة من ثوابت [SummaryLength](../../com.aspose.words/summarylength/).
### setSummaryLength(int value) {#setSummaryLength-int}
```
public void setSummaryLength(int value)
```


يسمح بتحديد طول الملخص. القيمة الافتراضية هي [SummaryLength.MEDIUM](../../com.aspose.words/summarylength/\#MEDIUM).

 **Examples:** 

يظهر كيفية تلخيص النص باستخدام نماذج OpenAI وGoogle.

```

 Document firstDoc = new Document(getMyDir() + "Big document.docx");
 Document secondDoc = new Document(getMyDir() + "Document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use OpenAI or Google generative language models.
 AiModel model = ((OpenAiModel)AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey)).withOrganization("Organization").withProject("Project");

 SummarizeOptions options = new SummarizeOptions();

 options.setSummaryLength(SummaryLength.SHORT);
 Document oneDocumentSummary = model.summarize(firstDoc, options);
 oneDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.One.docx");

 options.setSummaryLength(SummaryLength.LONG);
 Document multiDocumentSummary = model.summarize(new Document[] { firstDoc, secondDoc }, options);
 multiDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.Multi.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة int المقابلة. يجب أن تكون القيمة واحدة من ثوابت [SummaryLength](../../com.aspose.words/summarylength/). |

