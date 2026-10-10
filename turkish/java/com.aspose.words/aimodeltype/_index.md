---
title: "AiModelType"
linktitle: "AiModelType"
second_title: "Aspose.Words Java için"
description: "Java'da belge işleme iş akışına entegre edilebilen AiModel türlerini temsil eder."
type: docs
weight: 15
url: /tr/java/com.aspose.words/aimodeltype/
---

**Inheritance:**
java.lang.Object
```
public class AiModelType
```

Belge işleme iş akışına entegre edilebilen [AiModel](../../com.aspose.words/aimodel/) türlerini temsil eder.

 **Remarks:** 

Bu enum, özetleme, çeviri ve içerik üretimi gibi görevler için hangi büyük dil modelinin (LLM) kullanılacağını tanımlamak için kullanılır.

 **Examples:** 

OpenAI ve Google modellerini kullanarak metni nasıl özetleyeceğinizi gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CLAUDE_35_HAIKU](#CLAUDE-35-HAIKU) | Claude 3.5 Haiku üretken model türü. |
| [CLAUDE_35_SONNET](#CLAUDE-35-SONNET) | Claude 3.5 Sonnet üretken model türü. |
| [CLAUDE_3_HAIKU](#CLAUDE-3-HAIKU) | Claude 3 Haiku üretken model türü. |
| [CLAUDE_3_OPUS](#CLAUDE-3-OPUS) | Claude 3 Opus üretken model türü. |
| [CLAUDE_3_SONNET](#CLAUDE-3-SONNET) | Claude 3 Sonnet üretken model türü. |
| [GEMINI_FLASH_LATEST](#GEMINI-FLASH-LATEST) | Gemini Flash en son sürüm üretken model türü. |
| [GEMINI_PRO_LATEST](#GEMINI-PRO-LATEST) | Gemini Pro en son sürüm üretken model türü. |
| [GPT_35_TURBO](#GPT-35-TURBO) | GPT-3.5 Turbo üretken model türü. |
| [GPT_4_O](#GPT-4-O) | GPT-4o üretken model türü. |
| [GPT_4_O_MINI](#GPT-4-O-MINI) | GPT-4o mini üretken model türü. |
| [GPT_4_TURBO](#GPT-4-TURBO) | GPT-4 Turbo üretken model türü. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String aiModelTypeName)](#fromName-java.lang.String) |  |
| [getName(int aiModelType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int aiModelType)](#toString-int) |  |
### CLAUDE_35_HAIKU {#CLAUDE-35-HAIKU}
```
public static int CLAUDE_35_HAIKU
```


Claude 3.5 Haiku üretken model türü.

### CLAUDE_35_SONNET {#CLAUDE-35-SONNET}
```
public static int CLAUDE_35_SONNET
```


Claude 3.5 Sonnet üretken model türü.

### CLAUDE_3_HAIKU {#CLAUDE-3-HAIKU}
```
public static int CLAUDE_3_HAIKU
```


Claude 3 Haiku üretken model türü.

### CLAUDE_3_OPUS {#CLAUDE-3-OPUS}
```
public static int CLAUDE_3_OPUS
```


Claude 3 Opus üretken model türü.

### CLAUDE_3_SONNET {#CLAUDE-3-SONNET}
```
public static int CLAUDE_3_SONNET
```


Claude 3 Sonnet üretken model türü.

### GEMINI_FLASH_LATEST {#GEMINI-FLASH-LATEST}
```
public static int GEMINI_FLASH_LATEST
```


Gemini Flash en son sürüm üretken model türü.

### GEMINI_PRO_LATEST {#GEMINI-PRO-LATEST}
```
public static int GEMINI_PRO_LATEST
```


Gemini Pro en son sürüm üretken model türü.

### GPT_35_TURBO {#GPT-35-TURBO}
```
public static int GPT_35_TURBO
```


GPT-3.5 Turbo üretken model türü.

### GPT_4_O {#GPT-4-O}
```
public static int GPT_4_O
```


GPT-4o üretken model türü.

### GPT_4_O_MINI {#GPT-4-O-MINI}
```
public static int GPT_4_O_MINI
```


GPT-4o mini üretken model türü.

### GPT_4_TURBO {#GPT-4-TURBO}
```
public static int GPT_4_TURBO
```


GPT-4 Turbo üretken model türü.

### length {#length}
```
public static int length
```


### fromName(String aiModelTypeName) {#fromName-java.lang.String}
```
public static int fromName(String aiModelTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| aiModelTypeName | java.lang.String |  |

**Returns:**
int
### getName(int aiModelType) {#getName-int}
```
public static String getName(int aiModelType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| aiModelType | int |  |

**Returns:**
java.lang.String
