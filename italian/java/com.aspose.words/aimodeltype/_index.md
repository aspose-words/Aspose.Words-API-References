---
title: "AiModelType"
linktitle: "AiModelType"
second_title: "Aspose.Words per Java"
description: "Rappresenta i tipi di AiModel che possono essere integrati nel flusso di lavoro di elaborazione dei documenti in Java."
type: docs
weight: 15
url: /it/java/com.aspose.words/aimodeltype/
---

**Inheritance:**
java.lang.Object
```
public class AiModelType
```

Rappresenta i tipi di [AiModel](../../com.aspose.words/aimodel/) che possono essere integrati nel flusso di lavoro di elaborazione dei documenti.

 **Remarks:** 

Questa enumerazione è usata per definire quale modello di linguaggio di grandi dimensioni (LLM) dovrebbe essere utilizzato per attività come la sintesi, la traduzione e la generazione di contenuti.

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
| [CLAUDE_35_HAIKU](#CLAUDE-35-HAIKU) | Tipo di modello generativo Claude 3.5 Haiku. |
| [CLAUDE_35_SONNET](#CLAUDE-35-SONNET) | Tipo di modello generativo Claude 3.5 Sonnet. |
| [CLAUDE_3_HAIKU](#CLAUDE-3-HAIKU) | Tipo di modello generativo Claude 3 Haiku. |
| [CLAUDE_3_OPUS](#CLAUDE-3-OPUS) | Tipo di modello generativo Claude 3 Opus. |
| [CLAUDE_3_SONNET](#CLAUDE-3-SONNET) | Tipo di modello generativo Claude 3 Sonnet. |
| [GEMINI_FLASH_LATEST](#GEMINI-FLASH-LATEST) | Tipo di modello generativo Gemini Flash ultima versione. |
| [GEMINI_PRO_LATEST](#GEMINI-PRO-LATEST) | Tipo di modello generativo Gemini Pro ultima versione. |
| [GPT_35_TURBO](#GPT-35-TURBO) | Tipo di modello generativo GPT-3.5 Turbo. |
| [GPT_4_O](#GPT-4-O) | Tipo di modello generativo GPT-4o. |
| [GPT_4_O_MINI](#GPT-4-O-MINI) | Tipo di modello generativo GPT-4o mini. |
| [GPT_4_TURBO](#GPT-4-TURBO) | Tipo di modello generativo GPT-4 Turbo. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String aiModelTypeName)](#fromName-java.lang.String) |  |
| [getName(int aiModelType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int aiModelType)](#toString-int) |  |
### CLAUDE_35_HAIKU {#CLAUDE-35-HAIKU}
```
public static int CLAUDE_35_HAIKU
```


Tipo di modello generativo Claude 3.5 Haiku.

### CLAUDE_35_SONNET {#CLAUDE-35-SONNET}
```
public static int CLAUDE_35_SONNET
```


Tipo di modello generativo Claude 3.5 Sonnet.

### CLAUDE_3_HAIKU {#CLAUDE-3-HAIKU}
```
public static int CLAUDE_3_HAIKU
```


Tipo di modello generativo Claude 3 Haiku.

### CLAUDE_3_OPUS {#CLAUDE-3-OPUS}
```
public static int CLAUDE_3_OPUS
```


Tipo di modello generativo Claude 3 Opus.

### CLAUDE_3_SONNET {#CLAUDE-3-SONNET}
```
public static int CLAUDE_3_SONNET
```


Tipo di modello generativo Claude 3 Sonnet.

### GEMINI_FLASH_LATEST {#GEMINI-FLASH-LATEST}
```
public static int GEMINI_FLASH_LATEST
```


Tipo di modello generativo Gemini Flash ultima versione.

### GEMINI_PRO_LATEST {#GEMINI-PRO-LATEST}
```
public static int GEMINI_PRO_LATEST
```


Tipo di modello generativo Gemini Pro ultima versione.

### GPT_35_TURBO {#GPT-35-TURBO}
```
public static int GPT_35_TURBO
```


Tipo di modello generativo GPT-3.5 Turbo.

### GPT_4_O {#GPT-4-O}
```
public static int GPT_4_O
```


Tipo di modello generativo GPT-4o.

### GPT_4_O_MINI {#GPT-4-O-MINI}
```
public static int GPT_4_O_MINI
```


Tipo di modello generativo GPT-4o mini.

### GPT_4_TURBO {#GPT-4-TURBO}
```
public static int GPT_4_TURBO
```


Tipo di modello generativo GPT-4 Turbo.

### length {#length}
```
public static int length
```


### fromName(String aiModelTypeName) {#fromName-java.lang.String}
```
public static int fromName(String aiModelTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| aiModelTypeName | java.lang.String |  |

**Returns:**
int
### getName(int aiModelType) {#getName-int}
```
public static String getName(int aiModelType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| aiModelType | int |  |

**Returns:**
java.lang.String
