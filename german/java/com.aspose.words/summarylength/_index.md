---
title: "SummaryLength"
linktitle: "SummaryLength"
second_title: "Aspose.Words für Java"
description: "Enumeriert mögliche Längen der Zusammenfassung in Java."
type: docs
weight: 647
url: /de/java/com.aspose.words/summarylength/
---

**Inheritance:**
java.lang.Object
```
public class SummaryLength
```

Enumeriert mögliche Längen der Zusammenfassung.

 **Examples:** 

Zeigt, wie man Text mit OpenAI- und Google-Modellen zusammenfasst.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [LONG](#LONG) | Versuchen Sie, 7–10 Sätze zu erzeugen. |
| [MEDIUM](#MEDIUM) | Versuchen Sie, 5–6 Sätze zu erzeugen. |
| [SHORT](#SHORT) | Versuchen Sie, 3–4 Sätze zu erzeugen. |
| [VERY_LONG](#VERY-LONG) | Versuchen Sie, 11–20 Sätze zu erzeugen. |
| [VERY_SHORT](#VERY-SHORT) | Versuchen Sie, 1–2 Sätze zu erzeugen. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String summaryLengthName)](#fromName-java.lang.String) |  |
| [getName(int summaryLength)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int summaryLength)](#toString-int) |  |
### LONG {#LONG}
```
public static int LONG
```


Versuchen Sie, 7–10 Sätze zu erzeugen.

### MEDIUM {#MEDIUM}
```
public static int MEDIUM
```


Versuchen Sie, 5–6 Sätze zu erzeugen.

### SHORT {#SHORT}
```
public static int SHORT
```


Versuchen Sie, 3–4 Sätze zu erzeugen.

### VERY_LONG {#VERY-LONG}
```
public static int VERY_LONG
```


Versuchen Sie, 11–20 Sätze zu erzeugen.

### VERY_SHORT {#VERY-SHORT}
```
public static int VERY_SHORT
```


Versuchen Sie, 1–2 Sätze zu erzeugen.

### length {#length}
```
public static int length
```


### fromName(String summaryLengthName) {#fromName-java.lang.String}
```
public static int fromName(String summaryLengthName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| summaryLengthName | java.lang.String |  |

**Returns:**
int
### getName(int summaryLength) {#getName-int}
```
public static String getName(int summaryLength)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| summaryLength | int |  |

**Returns:**
java.lang.String
