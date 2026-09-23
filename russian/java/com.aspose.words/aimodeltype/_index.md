---
title: "AiModelType"
linktitle: "AiModelType"
second_title: "Aspose.Words для Java"
description: "Представляет типы AiModel, которые могут быть интегрированы в рабочий процесс обработки документов в Java."
type: docs
weight: 15
url: /ru/java/com.aspose.words/aimodeltype/
---

**Inheritance:**
java.lang.Object
```
public class AiModelType
```

Представляет типы [AiModel](../../com.aspose.words/aimodel/), которые могут быть интегрированы в рабочий процесс обработки документов.

 **Remarks:** 

Это перечисление используется для определения, какая крупная языковая модель (LLM) должна использоваться для задач, таких как суммирование, перевод и генерация контента.

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
| [CLAUDE_35_HAIKU](#CLAUDE-35-HAIKU) | Тип генеративной модели Claude 3.5 Haiku. |
| [CLAUDE_35_SONNET](#CLAUDE-35-SONNET) | Тип генеративной модели Claude 3.5 Sonnet. |
| [CLAUDE_3_HAIKU](#CLAUDE-3-HAIKU) | Тип генеративной модели Claude 3 Haiku. |
| [CLAUDE_3_OPUS](#CLAUDE-3-OPUS) | Тип генеративной модели Claude 3 Opus. |
| [CLAUDE_3_SONNET](#CLAUDE-3-SONNET) | Тип генеративной модели Claude 3 Sonnet. |
| [GEMINI_FLASH_LATEST](#GEMINI-FLASH-LATEST) | Тип генеративной модели Gemini Flash последнего выпуска. |
| [GEMINI_PRO_LATEST](#GEMINI-PRO-LATEST) | Тип генеративной модели Gemini Pro последнего выпуска. |
| [GPT_35_TURBO](#GPT-35-TURBO) | Тип генеративной модели GPT-3.5 Turbo. |
| [GPT_4_O](#GPT-4-O) | Тип генеративной модели GPT-4o. |
| [GPT_4_O_MINI](#GPT-4-O-MINI) | Тип генеративной модели GPT-4o mini. |
| [GPT_4_TURBO](#GPT-4-TURBO) | Тип генеративной модели GPT-4 Turbo. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String aiModelTypeName)](#fromName-java.lang.String) |  |
| [getName(int aiModelType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int aiModelType)](#toString-int) |  |
### CLAUDE_35_HAIKU {#CLAUDE-35-HAIKU}
```
public static int CLAUDE_35_HAIKU
```


Тип генеративной модели Claude 3.5 Haiku.

### CLAUDE_35_SONNET {#CLAUDE-35-SONNET}
```
public static int CLAUDE_35_SONNET
```


Тип генеративной модели Claude 3.5 Sonnet.

### CLAUDE_3_HAIKU {#CLAUDE-3-HAIKU}
```
public static int CLAUDE_3_HAIKU
```


Тип генеративной модели Claude 3 Haiku.

### CLAUDE_3_OPUS {#CLAUDE-3-OPUS}
```
public static int CLAUDE_3_OPUS
```


Тип генеративной модели Claude 3 Opus.

### CLAUDE_3_SONNET {#CLAUDE-3-SONNET}
```
public static int CLAUDE_3_SONNET
```


Тип генеративной модели Claude 3 Sonnet.

### GEMINI_FLASH_LATEST {#GEMINI-FLASH-LATEST}
```
public static int GEMINI_FLASH_LATEST
```


Тип генеративной модели Gemini Flash последнего выпуска.

### GEMINI_PRO_LATEST {#GEMINI-PRO-LATEST}
```
public static int GEMINI_PRO_LATEST
```


Тип генеративной модели Gemini Pro последнего выпуска.

### GPT_35_TURBO {#GPT-35-TURBO}
```
public static int GPT_35_TURBO
```


Тип генеративной модели GPT-3.5 Turbo.

### GPT_4_O {#GPT-4-O}
```
public static int GPT_4_O
```


Тип генеративной модели GPT-4o.

### GPT_4_O_MINI {#GPT-4-O-MINI}
```
public static int GPT_4_O_MINI
```


Тип генеративной модели GPT-4o mini.

### GPT_4_TURBO {#GPT-4-TURBO}
```
public static int GPT_4_TURBO
```


Тип генеративной модели GPT-4 Turbo.

### length {#length}
```
public static int length
```


### fromName(String aiModelTypeName) {#fromName-java.lang.String}
```
public static int fromName(String aiModelTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| aiModelTypeName | java.lang.String |  |

**Returns:**
int
### getName(int aiModelType) {#getName-int}
```
public static String getName(int aiModelType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| aiModelType | int |  |

**Returns:**
java.lang.String
