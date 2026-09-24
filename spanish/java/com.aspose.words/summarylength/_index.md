---
title: "SummaryLength"
linktitle: "SummaryLength"
second_title: "Aspose.Words para Java"
description: "Enumera las posibles longitudes del resumen en Java."
type: docs
weight: 647
url: /es/java/com.aspose.words/summarylength/
---

**Inheritance:**
java.lang.Object
```
public class SummaryLength
```

Enumera las posibles longitudes del resumen.

 **Examples:** 

Muestra cómo resumir texto usando los modelos de OpenAI y Google.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [LONG](#LONG) | Intenta generar 7-10 oraciones. |
| [MEDIUM](#MEDIUM) | Intenta generar 5-6 oraciones. |
| [SHORT](#SHORT) | Intenta generar 3-4 oraciones. |
| [VERY_LONG](#VERY-LONG) | Intenta generar 11-20 oraciones. |
| [VERY_SHORT](#VERY-SHORT) | Intenta generar 1-2 oraciones. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String summaryLengthName)](#fromName-java.lang.String) |  |
| [getName(int summaryLength)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int summaryLength)](#toString-int) |  |
### LONG {#LONG}
```
public static int LONG
```


Intenta generar 7-10 oraciones.

### MEDIUM {#MEDIUM}
```
public static int MEDIUM
```


Intenta generar 5-6 oraciones.

### SHORT {#SHORT}
```
public static int SHORT
```


Intenta generar 3-4 oraciones.

### VERY_LONG {#VERY-LONG}
```
public static int VERY_LONG
```


Intenta generar 11-20 oraciones.

### VERY_SHORT {#VERY-SHORT}
```
public static int VERY_SHORT
```


Intenta generar 1-2 oraciones.

### length {#length}
```
public static int length
```


### fromName(String summaryLengthName) {#fromName-java.lang.String}
```
public static int fromName(String summaryLengthName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| summaryLengthName | java.lang.String |  |

**Returns:**
int
### getName(int summaryLength) {#getName-int}
```
public static String getName(int summaryLength)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| summaryLength | int |  |

**Returns:**
java.lang.String
