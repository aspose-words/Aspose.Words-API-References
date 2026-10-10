---
title: "AnthropicAiModel"
linktitle: "AnthropicAiModel"
second_title: "Aspose.Words for Java"
description: "一个抽象类，表示在 Java 中的 Aspose.Words 与 Anthropic 的 AI 模型的集成。"
type: docs
weight: 16
url: /zh/java/com.aspose.words/anthropicaimodel/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.AiModel](../../com.aspose.words/aimodel/)
```
public abstract class AnthropicAiModel extends AiModel
```

一个抽象类，表示 Aspose.Words 与 Anthropic 的 AI 模型的集成。
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [AnthropicAiModel()](#AnthropicAiModel) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | 检查提供的文档的语法。 |
| [create(int modelType)](#create-int) |  |
| [getTimeout()](#getTimeout) | 获取在对 AI 模型的请求超时之前等待的毫秒数。 |
| [getUrl()](#getUrl) | 获取模型的 URL。 |
| [setTimeout(int value)](#setTimeout-int) | 设置在请求 AI 模型超时之前等待的毫秒数。 |
| [setUrl(String value)](#setUrl-java.lang.String) | 设置模型的 URL。 |
| [summarize(Document sourceDocument)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | 生成指定文档的摘要，并提供调整摘要长度的选项。 |
| [summarize(Document[] sourceDocuments)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | 为一组文档生成摘要，并提供控制摘要长度及其他设置的选项。 |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | 为模型设置指定的 API 密钥。 |
### AnthropicAiModel() {#AnthropicAiModel}
```
public AnthropicAiModel()
```


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


获取模型的 URL。默认值为 "https://api.anthropic.com/"。

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


设置模型的 URL。默认值为 "https://api.anthropic.com/"。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 模型的 URL。 |

### summarize(Document sourceDocument) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document sourceDocument)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public Document summarize(Document sourceDocument, SummarizeOptions options)
```


生成指定文档的摘要，并提供调整摘要长度的选项。此操作利用已连接的 AI 模型进行内容处理。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | 待摘要的文档。 |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | 用于控制摘要长度及其他参数的可选设置。 |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] sourceDocuments) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document[] sourceDocuments)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public Document summarize(Document[] sourceDocuments, SummarizeOptions options)
```


为一组文档生成摘要，并提供控制摘要长度及其他设置的选项。此方法利用已连接的 AI 模型处理数组中的每个文档。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) | 待摘要的一组文档。 |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | 用于控制摘要长度及其他参数的可选设置 |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### translate(Document sourceDocument, int targetLanguage) {#translate-com.aspose.words.Document-int}
```
public Document translate(Document sourceDocument, int targetLanguage)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| targetLanguage | int |  |

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
