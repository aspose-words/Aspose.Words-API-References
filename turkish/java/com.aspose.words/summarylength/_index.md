---
title: "SummaryLength"
linktitle: "SummaryLength"
second_title: "Aspose.Words Java için"
description: "Java'da özetin olası uzunluklarını listeler."
type: docs
weight: 647
url: /tr/java/com.aspose.words/summarylength/
---

**Inheritance:**
java.lang.Object
```
public class SummaryLength
```

Özetin olası uzunluklarını listeler.

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
| [LONG](#LONG) | 7-10 cümle üretmeyi deneyin. |
| [MEDIUM](#MEDIUM) | 5-6 cümle üretmeyi deneyin. |
| [SHORT](#SHORT) | 3-4 cümle üretmeyi deneyin. |
| [VERY_LONG](#VERY-LONG) | 11-20 cümle üretmeyi deneyin. |
| [VERY_SHORT](#VERY-SHORT) | 1-2 cümle üretmeyi deneyin. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String summaryLengthName)](#fromName-java.lang.String) |  |
| [getName(int summaryLength)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int summaryLength)](#toString-int) |  |
### LONG {#LONG}
```
public static int LONG
```


7-10 cümle üretmeyi deneyin.

### MEDIUM {#MEDIUM}
```
public static int MEDIUM
```


5-6 cümle üretmeyi deneyin.

### SHORT {#SHORT}
```
public static int SHORT
```


3-4 cümle üretmeyi deneyin.

### VERY_LONG {#VERY-LONG}
```
public static int VERY_LONG
```


11-20 cümle üretmeyi deneyin.

### VERY_SHORT {#VERY-SHORT}
```
public static int VERY_SHORT
```


1-2 cümle üretmeyi deneyin.

### length {#length}
```
public static int length
```


### fromName(String summaryLengthName) {#fromName-java.lang.String}
```
public static int fromName(String summaryLengthName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| summaryLengthName | java.lang.String |  |

**Returns:**
int
### getName(int summaryLength) {#getName-int}
```
public static String getName(int summaryLength)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| summaryLength | int |  |

**Returns:**
java.lang.String
