---
title: "SummaryLength"
linktitle: "SummaryLength"
second_title: "Aspose.Words per Java"
description: "Enumera le possibili lunghezze del riepilogo in Java."
type: docs
weight: 647
url: /it/java/com.aspose.words/summarylength/
---

**Inheritance:**
java.lang.Object
```
public class SummaryLength
```

Enumera le possibili lunghezze del riassunto.

 **Examples:** 

Mostra come riassumere il testo utilizzando i modelli OpenAI e Google.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [LONG](#LONG) | Prova a generare 7-10 frasi. |
| [MEDIUM](#MEDIUM) | Prova a generare 5-6 frasi. |
| [SHORT](#SHORT) | Prova a generare 3-4 frasi. |
| [VERY_LONG](#VERY-LONG) | Prova a generare 11-20 frasi. |
| [VERY_SHORT](#VERY-SHORT) | Prova a generare 1-2 frasi. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String summaryLengthName)](#fromName-java.lang.String) |  |
| [getName(int summaryLength)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int summaryLength)](#toString-int) |  |
### LONG {#LONG}
```
public static int LONG
```


Prova a generare 7-10 frasi.

### MEDIUM {#MEDIUM}
```
public static int MEDIUM
```


Prova a generare 5-6 frasi.

### SHORT {#SHORT}
```
public static int SHORT
```


Prova a generare 3-4 frasi.

### VERY_LONG {#VERY-LONG}
```
public static int VERY_LONG
```


Prova a generare 11-20 frasi.

### VERY_SHORT {#VERY-SHORT}
```
public static int VERY_SHORT
```


Prova a generare 1-2 frasi.

### length {#length}
```
public static int length
```


### fromName(String summaryLengthName) {#fromName-java.lang.String}
```
public static int fromName(String summaryLengthName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| summaryLengthName | java.lang.String |  |

**Returns:**
int
### getName(int summaryLength) {#getName-int}
```
public static String getName(int summaryLength)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| summaryLength | int |  |

**Returns:**
java.lang.String
