---
title: "GoogleAiModel"
linktitle: "GoogleAiModel"
second_title: "Aspose.Words for Java"
description: "表示 Aspose.Words 在 Java 中与 Google AI 模型 Gemini 集成的类。"
type: docs
weight: 361
url: /zh/java/com.aspose.words/googleaimodel/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.AiModel](../../com.aspose.words/aimodel/)
```
public class GoogleAiModel extends AiModel
```

表示 Aspose.Words 中 Google AI 模型（Gemini）集成的类。

 **Remarks:** 

请参阅 https://ai.google.dev/gemini-api/docs/models 获取 Gemini 模型的详细信息。

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

展示如何使用 Google AI 模型。

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [GoogleAiModel(String name)](#GoogleAiModel-java.lang.String) | 初始化一个新的 [GoogleAiModel](../../com.aspose.words/googleaimodel/) 类实例。 |
| [GoogleAiModel(String name, String apiKey)](#GoogleAiModel-java.lang.String-java.lang.String) | 初始化一个新的 [GoogleAiModel](../../com.aspose.words/googleaimodel/) 类实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | 检查提供的文档的语法。 |
| [create(int modelType)](#create-int) |  |
| [getTimeout()](#getTimeout) | 获取在对 AI 模型的请求超时之前等待的毫秒数。 |
| [getUrl()](#getUrl) | 获取模型的 URL。 |
| [setTimeout(int value)](#setTimeout-int) | 设置在请求 AI 模型超时之前等待的毫秒数。 |
| [setUrl(String value)](#setUrl-java.lang.String) | 设置模型的 URL。 |
| [summarize(Document doc)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document doc, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | 汇总指定的 [Document](../../com.aspose.words/document/) 对象。 |
| [summarize(Document[] docs)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document[] docs, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | 汇总指定的多个 [Document](../../com.aspose.words/document/) 对象。 |
| [translate(Document doc, int language)](#translate-com.aspose.words.Document-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | 为模型设置指定的 API 密钥。 |
### GoogleAiModel(String name) {#GoogleAiModel-java.lang.String}
```
public GoogleAiModel(String name)
```


初始化一个新的 [GoogleAiModel](../../com.aspose.words/googleaimodel/) 类实例。

 **Examples:** 

展示如何使用 Google AI 模型。

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 名称 | java.lang.String | 模型的名称。例如，gemini-2.5-flash。 |

### GoogleAiModel(String name, String apiKey) {#GoogleAiModel-java.lang.String-java.lang.String}
```
public GoogleAiModel(String name, String apiKey)
```


初始化一个新的 [GoogleAiModel](../../com.aspose.words/googleaimodel/) 类实例。

 **Examples:** 

展示如何使用 Google AI 模型。

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 名称 | java.lang.String | 模型的名称。例如，gemini-2.5-flash。 |
| apiKey | java.lang.String | 用于 Gemini API 的 API 密钥。请参阅 https://ai.google.dev/gemini-api/docs/api-key 获取详细信息。 |

### checkGrammar(Document sourceDocument, CheckGrammarOptions options) {#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions}
```
public Document checkGrammar(Document sourceDocument, CheckGrammarOptions options)
```


检查提供的文档的语法。此操作利用已连接的 AI 模型来检查文档的语法。

 **Examples:** 

展示如何检查文档的语法。

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use OpenAI generative language models.
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);

 CheckGrammarOptions grammarOptions = new CheckGrammarOptions();
 grammarOptions.setImproveStylistics(true);

 Document proofedDoc = model.checkGrammar(doc, grammarOptions);
 proofedDoc.save(getArtifactsDir() + "AI.AiGrammar.docx");
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | 正在检查语法的文档。 |
| options | [CheckGrammarOptions](../../com.aspose.words/checkgrammaroptions/) | 用于控制语法检查方式的可选设置。 |

**Returns:**
[Document](../../com.aspose.words/document/) - A new [Document](../../com.aspose.words/document/) with checked grammar.
### create(int modelType) {#create-int}
```
public static AiModel create(int modelType)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| modelType | int |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
### getTimeout() {#getTimeout}
```
public int getTimeout()
```


获取在请求 AI 模型超时之前等待的毫秒数。默认值为 100,000 毫秒（100 秒）。

 **Examples:** 

展示如何更改模型默认超时时间。

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value 100000ms.
 model.setTimeout(250000);
 
```

**Returns:**
int - 在请求 AI 模型超时之前等待的毫秒数。
### getUrl() {#getUrl}
```
public String getUrl()
```


获取模型的 URL。默认值为 "https://generativelanguage.googleapis.com/v1beta/models/"。

**Returns:**
java.lang.String - 模型的 URL。
### setTimeout(int value) {#setTimeout-int}
```
public void setTimeout(int value)
```


设置在请求 AI 模型超时之前等待的毫秒数。默认值为 100,000 毫秒（100 秒）。

 **Examples:** 

展示如何更改模型默认超时时间。

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value 100000ms.
 model.setTimeout(250000);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 在请求 AI 模型超时之前等待的毫秒数。 |

### setUrl(String value) {#setUrl-java.lang.String}
```
public void setUrl(String value)
```


设置模型的 URL。默认值为 "https://generativelanguage.googleapis.com/v1beta/models/"。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 模型的 URL。 |

### summarize(Document doc) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document doc)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document doc, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public Document summarize(Document doc, SummarizeOptions options)
```


汇总指定的 [Document](../../com.aspose.words/document/) 对象。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] docs) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document[] docs)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| docs | [Document\[\]](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] docs, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public Document summarize(Document[] docs, SummarizeOptions options)
```


汇总指定的多个 [Document](../../com.aspose.words/document/) 对象。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| docs | [Document\[\]](../../com.aspose.words/document/) |  |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### translate(Document doc, int language) {#translate-com.aspose.words.Document-int}
```
public Document translate(Document doc, int language)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |
| language | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### withApiKey(String apiKey) {#withApiKey-java.lang.String}
```
public AiModel withApiKey(String apiKey)
```


为模型设置指定的 API 密钥。

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
| apiKey | java.lang.String |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
