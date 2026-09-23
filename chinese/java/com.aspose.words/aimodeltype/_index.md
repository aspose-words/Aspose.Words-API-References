---
title: "AiModelType"
linktitle: "AiModelType"
second_title: "Aspose.Words for Java"
description: "表示可以在 Java 中集成到文档处理工作流的 AiModel 类型。"
type: docs
weight: 15
url: /zh/java/com.aspose.words/aimodeltype/
---

**Inheritance:**
java.lang.Object
```
public class AiModelType
```

表示可以集成到文档处理工作流的 [AiModel](../../com.aspose.words/aimodel/) 类型。

 **Remarks:** 

此枚举用于定义在摘要、翻译和内容生成等任务中应使用的 大语言模型 (LLM)。

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
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [CLAUDE_35_HAIKU](#CLAUDE-35-HAIKU) | Claude 3.5 Haiku 生成模型类型。 |
| [CLAUDE_35_SONNET](#CLAUDE-35-SONNET) | Claude 3.5 Sonnet 生成模型类型。 |
| [CLAUDE_3_HAIKU](#CLAUDE-3-HAIKU) | Claude 3 Haiku 生成模型类型。 |
| [CLAUDE_3_OPUS](#CLAUDE-3-OPUS) | Claude 3 Opus 生成模型类型。 |
| [CLAUDE_3_SONNET](#CLAUDE-3-SONNET) | Claude 3 Sonnet 生成模型类型。 |
| [GEMINI_FLASH_LATEST](#GEMINI-FLASH-LATEST) | Gemini Flash 最新发布的生成模型类型。 |
| [GEMINI_PRO_LATEST](#GEMINI-PRO-LATEST) | Gemini Pro 最新发布的生成模型类型。 |
| [GPT_35_TURBO](#GPT-35-TURBO) | GPT-3.5 Turbo 生成模型类型。 |
| [GPT_4_O](#GPT-4-O) | GPT-4o 生成模型类型。 |
| [GPT_4_O_MINI](#GPT-4-O-MINI) | GPT-4o mini 生成模型类型。 |
| [GPT_4_TURBO](#GPT-4-TURBO) | GPT-4 Turbo 生成模型类型。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String aiModelTypeName)](#fromName-java.lang.String) |  |
| [getName(int aiModelType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int aiModelType)](#toString-int) |  |
### CLAUDE_35_HAIKU {#CLAUDE-35-HAIKU}
```
public static int CLAUDE_35_HAIKU
```


Claude 3.5 Haiku 生成模型类型。

### CLAUDE_35_SONNET {#CLAUDE-35-SONNET}
```
public static int CLAUDE_35_SONNET
```


Claude 3.5 Sonnet 生成模型类型。

### CLAUDE_3_HAIKU {#CLAUDE-3-HAIKU}
```
public static int CLAUDE_3_HAIKU
```


Claude 3 Haiku 生成模型类型。

### CLAUDE_3_OPUS {#CLAUDE-3-OPUS}
```
public static int CLAUDE_3_OPUS
```


Claude 3 Opus 生成模型类型。

### CLAUDE_3_SONNET {#CLAUDE-3-SONNET}
```
public static int CLAUDE_3_SONNET
```


Claude 3 Sonnet 生成模型类型。

### GEMINI_FLASH_LATEST {#GEMINI-FLASH-LATEST}
```
public static int GEMINI_FLASH_LATEST
```


Gemini Flash 最新发布的生成模型类型。

### GEMINI_PRO_LATEST {#GEMINI-PRO-LATEST}
```
public static int GEMINI_PRO_LATEST
```


Gemini Pro 最新发布的生成模型类型。

### GPT_35_TURBO {#GPT-35-TURBO}
```
public static int GPT_35_TURBO
```


GPT-3.5 Turbo 生成模型类型。

### GPT_4_O {#GPT-4-O}
```
public static int GPT_4_O
```


GPT-4o 生成模型类型。

### GPT_4_O_MINI {#GPT-4-O-MINI}
```
public static int GPT_4_O_MINI
```


GPT-4o mini 生成模型类型。

### GPT_4_TURBO {#GPT-4-TURBO}
```
public static int GPT_4_TURBO
```


GPT-4 Turbo 生成模型类型。

### length {#length}
```
public static int length
```


### fromName(String aiModelTypeName) {#fromName-java.lang.String}
```
public static int fromName(String aiModelTypeName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| aiModelTypeName | java.lang.String |  |

**Returns:**
int
### getName(int aiModelType) {#getName-int}
```
public static String getName(int aiModelType)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| aiModelType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int aiModelType) {#toString-int}
```
public static String toString(int aiModelType)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| aiModelType | int |  |

**Returns:**
java.lang.String
