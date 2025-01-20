---
title: AiModelType
linktitle: AiModelType
second_title: Aspose.Words for Java
description: Represents the types of AiModel that can be integrated into the document processing workflow in Java.
type: docs
weight: 15
url: /java/com.aspose.words/aimodeltype/
---

**Inheritance:**
java.lang.Object
```
public class AiModelType
```

Represents the types of [AiModel](../../com.aspose.words/aimodel/) that can be integrated into the document processing workflow.

 **Remarks:** 

This enumeration is used to define which large language model (LLM) should be utilized for tasks such as summarization, translation, and content generation.

 **Examples:** 

Shows how to summarize text using OpenAI and Google models.

```

 Document firstDoc = new Document(getMyDir() + "Big document.docx");
 Document secondDoc = new Document(getMyDir() + "Document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use OpenAI or Google generative language models.
 IAiModelText model = ((OpenAiModel)AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey)).withOrganization("Organization").withProject("Project");

 SummarizeOptions options = new SummarizeOptions();
 options.setSummaryLength(SummaryLength.SHORT);
 Document oneDocumentSummary = model.summarize(firstDoc, options);
 oneDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.One.docx");

 options = new SummarizeOptions();
 options.setSummaryLength(SummaryLength.LONG);
 Document multiDocumentSummary = model.summarize(new Document[] { firstDoc, secondDoc }, options);
 multiDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.Multi.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [GEMINI_15_FLASH](#GEMINI-15-FLASH) | Gemini 1.5 Flash generative model type. |
| [GEMINI_15_FLASH_8_B](#GEMINI-15-FLASH-8-B) | Gemini 1.5 Flash-8B generative model type. |
| [GEMINI_15_PRO](#GEMINI-15-PRO) | Gemini 1.5 Pro generative model type. |
| [GPT_35_TURBO](#GPT-35-TURBO) | GPT-3.5 Turbo generative model type. |
| [GPT_4_O](#GPT-4-O) | GPT-4o generative model type. |
| [GPT_4_O_MINI](#GPT-4-O-MINI) | GPT-4o mini generative model type. |
| [GPT_4_TURBO](#GPT-4-TURBO) | GPT-4 Turbo generative model type. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String aiModelTypeName)](#fromName-java.lang.String) |  |
| [getName(int aiModelType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int aiModelType)](#toString-int) |  |
### GEMINI_15_FLASH {#GEMINI-15-FLASH}
```
public static int GEMINI_15_FLASH
```


Gemini 1.5 Flash generative model type.

### GEMINI_15_FLASH_8_B {#GEMINI-15-FLASH-8-B}
```
public static int GEMINI_15_FLASH_8_B
```


Gemini 1.5 Flash-8B generative model type.

### GEMINI_15_PRO {#GEMINI-15-PRO}
```
public static int GEMINI_15_PRO
```


Gemini 1.5 Pro generative model type.

### GPT_35_TURBO {#GPT-35-TURBO}
```
public static int GPT_35_TURBO
```


GPT-3.5 Turbo generative model type.

### GPT_4_O {#GPT-4-O}
```
public static int GPT_4_O
```


GPT-4o generative model type.

### GPT_4_O_MINI {#GPT-4-O-MINI}
```
public static int GPT_4_O_MINI
```


GPT-4o mini generative model type.

### GPT_4_TURBO {#GPT-4-TURBO}
```
public static int GPT_4_TURBO
```


GPT-4 Turbo generative model type.

### length {#length}
```
public static int length
```


### fromName(String aiModelTypeName) {#fromName-java.lang.String}
```
public static int fromName(String aiModelTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| aiModelTypeName | java.lang.String |  |

**Returns:**
int
### getName(int aiModelType) {#getName-int}
```
public static String getName(int aiModelType)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| aiModelType | int |  |

**Returns:**
java.lang.String
