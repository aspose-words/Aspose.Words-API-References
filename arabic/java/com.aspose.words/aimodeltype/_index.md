---
title: "AiModelType"
linktitle: "AiModelType"
second_title: "Aspose.Words لـ Java"
description: "يمثل أنواع AiModel التي يمكن دمجها في سير عمل معالجة المستندات في Java."
type: docs
weight: 15
url: /ar/java/com.aspose.words/aimodeltype/
---

**Inheritance:**
java.lang.Object
```
public class AiModelType
```

يمثل أنواع [AiModel](../../com.aspose.words/aimodel/) التي يمكن دمجها في سير عمل معالجة المستندات.

 **Remarks:** 

يُستخدم هذا التعداد لتحديد أي نموذج لغة كبير (LLM) يجب استخدامه للمهام مثل التلخيص، والترجمة، وتوليد المحتوى.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [CLAUDE_35_HAIKU](#CLAUDE-35-HAIKU) | نوع النموذج التوليدي Claude 3.5 Haiku. |
| [CLAUDE_35_SONNET](#CLAUDE-35-SONNET) | نوع النموذج التوليدي Claude 3.5 Sonnet. |
| [CLAUDE_3_HAIKU](#CLAUDE-3-HAIKU) | نوع النموذج التوليدي Claude 3 Haiku. |
| [CLAUDE_3_OPUS](#CLAUDE-3-OPUS) | نوع النموذج التوليدي Claude 3 Opus. |
| [CLAUDE_3_SONNET](#CLAUDE-3-SONNET) | نوع النموذج التوليدي Claude 3 Sonnet. |
| [GEMINI_FLASH_LATEST](#GEMINI-FLASH-LATEST) | نوع النموذج التوليدي Gemini Flash الإصدار الأخير. |
| [GEMINI_PRO_LATEST](#GEMINI-PRO-LATEST) | نوع النموذج التوليدي Gemini Pro الإصدار الأخير. |
| [GPT_35_TURBO](#GPT-35-TURBO) | نوع النموذج التوليدي GPT-3.5 Turbo. |
| [GPT_4_O](#GPT-4-O) | نوع النموذج التوليدي GPT-4o. |
| [GPT_4_O_MINI](#GPT-4-O-MINI) | نوع نموذج توليدي GPT-4o mini. |
| [GPT_4_TURBO](#GPT-4-TURBO) | نوع نموذج توليدي GPT-4 Turbo. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String aiModelTypeName)](#fromName-java.lang.String) |  |
| [getName(int aiModelType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int aiModelType)](#toString-int) |  |
### CLAUDE_35_HAIKU {#CLAUDE-35-HAIKU}
```
public static int CLAUDE_35_HAIKU
```


نوع النموذج التوليدي Claude 3.5 Haiku.

### CLAUDE_35_SONNET {#CLAUDE-35-SONNET}
```
public static int CLAUDE_35_SONNET
```


نوع النموذج التوليدي Claude 3.5 Sonnet.

### CLAUDE_3_HAIKU {#CLAUDE-3-HAIKU}
```
public static int CLAUDE_3_HAIKU
```


نوع النموذج التوليدي Claude 3 Haiku.

### CLAUDE_3_OPUS {#CLAUDE-3-OPUS}
```
public static int CLAUDE_3_OPUS
```


نوع النموذج التوليدي Claude 3 Opus.

### CLAUDE_3_SONNET {#CLAUDE-3-SONNET}
```
public static int CLAUDE_3_SONNET
```


نوع النموذج التوليدي Claude 3 Sonnet.

### GEMINI_FLASH_LATEST {#GEMINI-FLASH-LATEST}
```
public static int GEMINI_FLASH_LATEST
```


نوع النموذج التوليدي Gemini Flash الإصدار الأخير.

### GEMINI_PRO_LATEST {#GEMINI-PRO-LATEST}
```
public static int GEMINI_PRO_LATEST
```


نوع النموذج التوليدي Gemini Pro الإصدار الأخير.

### GPT_35_TURBO {#GPT-35-TURBO}
```
public static int GPT_35_TURBO
```


نوع النموذج التوليدي GPT-3.5 Turbo.

### GPT_4_O {#GPT-4-O}
```
public static int GPT_4_O
```


نوع النموذج التوليدي GPT-4o.

### GPT_4_O_MINI {#GPT-4-O-MINI}
```
public static int GPT_4_O_MINI
```


نوع نموذج توليدي GPT-4o mini.

### GPT_4_TURBO {#GPT-4-TURBO}
```
public static int GPT_4_TURBO
```


نوع نموذج توليدي GPT-4 Turbo.

### length {#length}
```
public static int length
```


### fromName(String aiModelTypeName) {#fromName-java.lang.String}
```
public static int fromName(String aiModelTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| aiModelTypeName | java.lang.String |  |

**Returns:**
int
### getName(int aiModelType) {#getName-int}
```
public static String getName(int aiModelType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| aiModelType | int |  |

**Returns:**
java.lang.String
