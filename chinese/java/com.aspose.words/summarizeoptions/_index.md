---
title: "SummarizeOptions"
linktitle: "SummarizeOptions"
second_title: "Aspose.Words for Java"
description: "允许在 Java 中指定用于摘要文档内容的各种选项。"
type: docs
weight: 646
url: /zh/java/com.aspose.words/summarizeoptions/
---

**Inheritance:**
java.lang.Object
```
public class SummarizeOptions
```

允许指定用于摘要文档内容的各种选项。

 **Examples:** 

展示如何使用 OpenAI 和 Google 模型对文本进行摘要。

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
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [SummarizeOptions()](#SummarizeOptions) | 初始化一个新的 [SummarizeOptions](../../com.aspose.words/summarizeoptions/) 类实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [getSummaryLength()](#getSummaryLength) | 允许指定摘要长度。 |
| [setSummaryLength(int value)](#setSummaryLength-int) | 允许指定摘要长度。 |
### SummarizeOptions() {#SummarizeOptions}
```
public SummarizeOptions()
```


初始化一个新的 [SummarizeOptions](../../com.aspose.words/summarizeoptions/) 类实例。

 **Examples:** 

展示如何使用 OpenAI 和 Google 模型对文本进行摘要。

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


允许指定摘要长度。默认值为 [SummaryLength.MEDIUM](../../com.aspose.words/summarylength/\#MEDIUM)。

 **Examples:** 

展示如何使用 OpenAI 和 Google 模型对文本进行摘要。

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
int - 对应的  int  值。返回的值是 [SummaryLength](../../com.aspose.words/summarylength/) 常量之一。
### setSummaryLength(int value) {#setSummaryLength-int}
```
public void setSummaryLength(int value)
```


允许指定摘要长度。默认值为 [SummaryLength.MEDIUM](../../com.aspose.words/summarylength/\#MEDIUM)。

 **Examples:** 

展示如何使用 OpenAI 和 Google 模型对文本进行摘要。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的  int  值。该值必须是 [SummaryLength](../../com.aspose.words/summarylength/) 常量之一。 |

