---
title: "SummaryLength"
linktitle: "SummaryLength"
second_title: "Aspose.Words pour Java"
description: "Énumère les longueurs possibles du résumé en Java."
type: docs
weight: 647
url: /fr/java/com.aspose.words/summarylength/
---

**Inheritance:**
java.lang.Object
```
public class SummaryLength
```

Énumère les longueurs possibles du résumé.

 **Examples:** 

Montre comment résumer le texte en utilisant les modèles OpenAI et Google.

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
## Champs

| Champ | Description |
| --- | --- |
| [LONG](#LONG) | Essayez de générer 7 à 10 phrases. |
| [MEDIUM](#MEDIUM) | Essayez de générer 5 à 6 phrases. |
| [SHORT](#SHORT) | Essayez de générer 3 à 4 phrases. |
| [VERY_LONG](#VERY-LONG) | Essayez de générer 11 à 20 phrases. |
| [VERY_SHORT](#VERY-SHORT) | Essayez de générer 1 à 2 phrases. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String summaryLengthName)](#fromName-java.lang.String) |  |
| [getName(int summaryLength)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int summaryLength)](#toString-int) |  |
### LONG {#LONG}
```
public static int LONG
```


Essayez de générer 7 à 10 phrases.

### MEDIUM {#MEDIUM}
```
public static int MEDIUM
```


Essayez de générer 5 à 6 phrases.

### SHORT {#SHORT}
```
public static int SHORT
```


Essayez de générer 3 à 4 phrases.

### VERY_LONG {#VERY-LONG}
```
public static int VERY_LONG
```


Essayez de générer 11 à 20 phrases.

### VERY_SHORT {#VERY-SHORT}
```
public static int VERY_SHORT
```


Essayez de générer 1 à 2 phrases.

### length {#length}
```
public static int length
```


### fromName(String summaryLengthName) {#fromName-java.lang.String}
```
public static int fromName(String summaryLengthName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| summaryLengthName | java.lang.String |  |

**Returns:**
int
### getName(int summaryLength) {#getName-int}
```
public static String getName(int summaryLength)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| summaryLength | int |  |

**Returns:**
java.lang.String
