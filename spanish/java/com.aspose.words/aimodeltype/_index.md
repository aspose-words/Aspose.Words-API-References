---
title: "AiModelType"
linktitle: "AiModelType"
second_title: "Aspose.Words para Java"
description: "Representa los tipos de AiModel que pueden integrarse en el flujo de trabajo de procesamiento de documentos en Java."
type: docs
weight: 15
url: /es/java/com.aspose.words/aimodeltype/
---

**Inheritance:**
java.lang.Object
```
public class AiModelType
```

Representa los tipos de [AiModel](../../com.aspose.words/aimodel/) que pueden integrarse en el flujo de trabajo de procesamiento de documentos.

 **Remarks:** 

Esta enumeración se utiliza para definir qué modelo de lenguaje grande (LLM) debe emplearse para tareas como resumen, traducción y generación de contenido.

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
| [CLAUDE_35_HAIKU](#CLAUDE-35-HAIKU) | Tipo de modelo generativo Claude 3.5 Haiku. |
| [CLAUDE_35_SONNET](#CLAUDE-35-SONNET) | Tipo de modelo generativo Claude 3.5 Sonnet. |
| [CLAUDE_3_HAIKU](#CLAUDE-3-HAIKU) | Tipo de modelo generativo Claude 3 Haiku. |
| [CLAUDE_3_OPUS](#CLAUDE-3-OPUS) | Tipo de modelo generativo Claude 3 Opus. |
| [CLAUDE_3_SONNET](#CLAUDE-3-SONNET) | Tipo de modelo generativo Claude 3 Sonnet. |
| [GEMINI_FLASH_LATEST](#GEMINI-FLASH-LATEST) | Tipo de modelo generativo Gemini Flash de la última versión. |
| [GEMINI_PRO_LATEST](#GEMINI-PRO-LATEST) | Tipo de modelo generativo Gemini Pro de la última versión. |
| [GPT_35_TURBO](#GPT-35-TURBO) | Tipo de modelo generativo GPT-3.5 Turbo. |
| [GPT_4_O](#GPT-4-O) | Tipo de modelo generativo GPT-4o. |
| [GPT_4_O_MINI](#GPT-4-O-MINI) | Tipo de modelo generativo GPT-4o mini. |
| [GPT_4_TURBO](#GPT-4-TURBO) | Tipo de modelo generativo GPT-4 Turbo. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String aiModelTypeName)](#fromName-java.lang.String) |  |
| [getName(int aiModelType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int aiModelType)](#toString-int) |  |
### CLAUDE_35_HAIKU {#CLAUDE-35-HAIKU}
```
public static int CLAUDE_35_HAIKU
```


Tipo de modelo generativo Claude 3.5 Haiku.

### CLAUDE_35_SONNET {#CLAUDE-35-SONNET}
```
public static int CLAUDE_35_SONNET
```


Tipo de modelo generativo Claude 3.5 Sonnet.

### CLAUDE_3_HAIKU {#CLAUDE-3-HAIKU}
```
public static int CLAUDE_3_HAIKU
```


Tipo de modelo generativo Claude 3 Haiku.

### CLAUDE_3_OPUS {#CLAUDE-3-OPUS}
```
public static int CLAUDE_3_OPUS
```


Tipo de modelo generativo Claude 3 Opus.

### CLAUDE_3_SONNET {#CLAUDE-3-SONNET}
```
public static int CLAUDE_3_SONNET
```


Tipo de modelo generativo Claude 3 Sonnet.

### GEMINI_FLASH_LATEST {#GEMINI-FLASH-LATEST}
```
public static int GEMINI_FLASH_LATEST
```


Tipo de modelo generativo Gemini Flash de la última versión.

### GEMINI_PRO_LATEST {#GEMINI-PRO-LATEST}
```
public static int GEMINI_PRO_LATEST
```


Tipo de modelo generativo Gemini Pro de la última versión.

### GPT_35_TURBO {#GPT-35-TURBO}
```
public static int GPT_35_TURBO
```


Tipo de modelo generativo GPT-3.5 Turbo.

### GPT_4_O {#GPT-4-O}
```
public static int GPT_4_O
```


Tipo de modelo generativo GPT-4o.

### GPT_4_O_MINI {#GPT-4-O-MINI}
```
public static int GPT_4_O_MINI
```


Tipo de modelo generativo GPT-4o mini.

### GPT_4_TURBO {#GPT-4-TURBO}
```
public static int GPT_4_TURBO
```


Tipo de modelo generativo GPT-4 Turbo.

### length {#length}
```
public static int length
```


### fromName(String aiModelTypeName) {#fromName-java.lang.String}
```
public static int fromName(String aiModelTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| aiModelTypeName | java.lang.String |  |

**Returns:**
int
### getName(int aiModelType) {#getName-int}
```
public static String getName(int aiModelType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| aiModelType | int |  |

**Returns:**
java.lang.String
