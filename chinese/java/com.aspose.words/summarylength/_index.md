---
title: "SummaryLength"
linktitle: "SummaryLength"
second_title: "Aspose.Words for Java"
description: "在 Java 中枚举摘要的可能长度。"
type: docs
weight: 647
url: /zh/java/com.aspose.words/summarylength/
---

**Inheritance:**
java.lang.Object
```
public class SummaryLength
```

枚举摘要的可能长度。

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
| [LONG](#LONG) | 尝试生成 7-10 句。 |
| [MEDIUM](#MEDIUM) | 尝试生成 5-6 句。 |
| [SHORT](#SHORT) | 尝试生成 3-4 句。 |
| [VERY_LONG](#VERY-LONG) | 尝试生成 11-20 句。 |
| [VERY_SHORT](#VERY-SHORT) | 尝试生成 1-2 句。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String summaryLengthName)](#fromName-java.lang.String) |  |
| [getName(int summaryLength)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int summaryLength)](#toString-int) |  |
### LONG {#LONG}
```
public static int LONG
```


尝试生成 7-10 句。

### MEDIUM {#MEDIUM}
```
public static int MEDIUM
```


尝试生成 5-6 句。

### SHORT {#SHORT}
```
public static int SHORT
```


尝试生成 3-4 句。

### VERY_LONG {#VERY-LONG}
```
public static int VERY_LONG
```


尝试生成 11-20 句。

### VERY_SHORT {#VERY-SHORT}
```
public static int VERY_SHORT
```


尝试生成 1-2 句。

### length {#length}
```
public static int length
```


### fromName(String summaryLengthName) {#fromName-java.lang.String}
```
public static int fromName(String summaryLengthName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| summaryLengthName | java.lang.String |  |

**Returns:**
int
### getName(int summaryLength) {#getName-int}
```
public static String getName(int summaryLength)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| summaryLength | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int summaryLength) {#toString-int}
```
public static String toString(int summaryLength)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| summaryLength | int |  |

**Returns:**
java.lang.String
