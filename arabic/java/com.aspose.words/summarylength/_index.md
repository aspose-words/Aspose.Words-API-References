---
title: "SummaryLength"
linktitle: "SummaryLength"
second_title: "Aspose.Words لـ Java"
description: "يعدّ الأطوال الممكنة للملخص في Java."
type: docs
weight: 647
url: /ar/java/com.aspose.words/summarylength/
---

**Inheritance:**
java.lang.Object
```
public class SummaryLength
```

يسرد الأطوال الممكنة للملخص.

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
| [LONG](#LONG) | حاول توليد 7-10 جمل. |
| [MEDIUM](#MEDIUM) | حاول توليد 5-6 جمل. |
| [SHORT](#SHORT) | حاول توليد 3-4 جمل. |
| [VERY_LONG](#VERY-LONG) | حاول توليد 11-20 جملة. |
| [VERY_SHORT](#VERY-SHORT) | حاول توليد 1-2 جملة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String summaryLengthName)](#fromName-java.lang.String) |  |
| [getName(int summaryLength)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int summaryLength)](#toString-int) |  |
### LONG {#LONG}
```
public static int LONG
```


حاول توليد 7-10 جمل.

### MEDIUM {#MEDIUM}
```
public static int MEDIUM
```


حاول توليد 5-6 جمل.

### SHORT {#SHORT}
```
public static int SHORT
```


حاول توليد 3-4 جمل.

### VERY_LONG {#VERY-LONG}
```
public static int VERY_LONG
```


حاول توليد 11-20 جملة.

### VERY_SHORT {#VERY-SHORT}
```
public static int VERY_SHORT
```


حاول توليد 1-2 جملة.

### length {#length}
```
public static int length
```


### fromName(String summaryLengthName) {#fromName-java.lang.String}
```
public static int fromName(String summaryLengthName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| summaryLengthName | java.lang.String |  |

**Returns:**
int
### getName(int summaryLength) {#getName-int}
```
public static String getName(int summaryLength)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| summaryLength | int |  |

**Returns:**
java.lang.String
