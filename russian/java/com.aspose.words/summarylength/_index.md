---
title: "SummaryLength"
linktitle: "SummaryLength"
second_title: "Aspose.Words для Java"
description: "Перечисляет возможные длины резюме в Java."
type: docs
weight: 647
url: /ru/java/com.aspose.words/summarylength/
---

**Inheritance:**
java.lang.Object
```
public class SummaryLength
```

Перечисляет возможные длины резюме.

 **Examples:** 

Показывает, как суммировать текст с использованием моделей OpenAI и Google.

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
## Поля

| Поле | Описание |
| --- | --- |
| [LONG](#LONG) | Попробуйте сгенерировать 7‑10 предложений. |
| [MEDIUM](#MEDIUM) | Попробуйте сгенерировать 5‑6 предложений. |
| [SHORT](#SHORT) | Попробуйте сгенерировать 3‑4 предложения. |
| [VERY_LONG](#VERY-LONG) | Попробуйте сгенерировать 11‑20 предложений. |
| [VERY_SHORT](#VERY-SHORT) | Попробуйте сгенерировать 1‑2 предложения. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String summaryLengthName)](#fromName-java.lang.String) |  |
| [getName(int summaryLength)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int summaryLength)](#toString-int) |  |
### LONG {#LONG}
```
public static int LONG
```


Попробуйте сгенерировать 7‑10 предложений.

### MEDIUM {#MEDIUM}
```
public static int MEDIUM
```


Попробуйте сгенерировать 5‑6 предложений.

### SHORT {#SHORT}
```
public static int SHORT
```


Попробуйте сгенерировать 3‑4 предложения.

### VERY_LONG {#VERY-LONG}
```
public static int VERY_LONG
```


Попробуйте сгенерировать 11‑20 предложений.

### VERY_SHORT {#VERY-SHORT}
```
public static int VERY_SHORT
```


Попробуйте сгенерировать 1‑2 предложения.

### length {#length}
```
public static int length
```


### fromName(String summaryLengthName) {#fromName-java.lang.String}
```
public static int fromName(String summaryLengthName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| summaryLengthName | java.lang.String |  |

**Returns:**
int
### getName(int summaryLength) {#getName-int}
```
public static String getName(int summaryLength)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| summaryLength | int |  |

**Returns:**
java.lang.String
