---
title: SummaryLength
linktitle: SummaryLength
second_title: Aspose.Words for Java
description: Enumerates possible lengths of summary in Java.
type: docs
weight: 645
url: /java/com.aspose.words/summarylength/
---

**Inheritance:**
java.lang.Object
```
public class SummaryLength
```

Enumerates possible lengths of summary.

 **Examples:** 

Shows how to summarize text using OpenAI and Google models.

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
## Fields

| Field | Description |
| --- | --- |
| [LONG](#LONG) | Try to generate 7-10 sentences. |
| [MEDIUM](#MEDIUM) | Try to generate 5-6 sentences. |
| [SHORT](#SHORT) | Try to generate 3-4 sentences. |
| [VERY_LONG](#VERY-LONG) | Try to generate 11-20 sentences. |
| [VERY_SHORT](#VERY-SHORT) | Try to generate 1-2 sentences. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String summaryLengthName)](#fromName-java.lang.String) |  |
| [getName(int summaryLength)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int summaryLength)](#toString-int) |  |
### LONG {#LONG}
```
public static int LONG
```


Try to generate 7-10 sentences.

### MEDIUM {#MEDIUM}
```
public static int MEDIUM
```


Try to generate 5-6 sentences.

### SHORT {#SHORT}
```
public static int SHORT
```


Try to generate 3-4 sentences.

### VERY_LONG {#VERY-LONG}
```
public static int VERY_LONG
```


Try to generate 11-20 sentences.

### VERY_SHORT {#VERY-SHORT}
```
public static int VERY_SHORT
```


Try to generate 1-2 sentences.

### length {#length}
```
public static int length
```


### fromName(String summaryLengthName) {#fromName-java.lang.String}
```
public static int fromName(String summaryLengthName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| summaryLengthName | java.lang.String |  |

**Returns:**
int
### getName(int summaryLength) {#getName-int}
```
public static String getName(int summaryLength)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| summaryLength | int |  |

**Returns:**
java.lang.String
