---
title: "AiModelType"
linktitle: "AiModelType"
second_title: "Aspose.Words pour Java"
description: "Représente les types d'AiModel qui peuvent être intégrés dans le flux de travail de traitement de documents en Java."
type: docs
weight: 15
url: /fr/java/com.aspose.words/aimodeltype/
---

**Inheritance:**
java.lang.Object
```
public class AiModelType
```

Représente les types de [AiModel](../../com.aspose.words/aimodel/) qui peuvent être intégrés dans le flux de travail de traitement de documents.

 **Remarks:** 

Cette énumération est utilisée pour définir quel grand modèle de langage (LLM) doit être utilisé pour des tâches telles que le résumé, la traduction et la génération de contenu.

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
| [CLAUDE_35_HAIKU](#CLAUDE-35-HAIKU) | Type de modèle génératif Claude 3.5 Haiku. |
| [CLAUDE_35_SONNET](#CLAUDE-35-SONNET) | Type de modèle génératif Claude 3.5 Sonnet. |
| [CLAUDE_3_HAIKU](#CLAUDE-3-HAIKU) | Type de modèle génératif Claude 3 Haiku. |
| [CLAUDE_3_OPUS](#CLAUDE-3-OPUS) | Type de modèle génératif Claude 3 Opus. |
| [CLAUDE_3_SONNET](#CLAUDE-3-SONNET) | Type de modèle génératif Claude 3 Sonnet. |
| [GEMINI_FLASH_LATEST](#GEMINI-FLASH-LATEST) | Type de modèle génératif Gemini Flash dernière version. |
| [GEMINI_PRO_LATEST](#GEMINI-PRO-LATEST) | Type de modèle génératif Gemini Pro dernière version. |
| [GPT_35_TURBO](#GPT-35-TURBO) | Type de modèle génératif GPT-3.5 Turbo. |
| [GPT_4_O](#GPT-4-O) | Type de modèle génératif GPT-4o. |
| [GPT_4_O_MINI](#GPT-4-O-MINI) | Type de modèle génératif GPT-4o mini. |
| [GPT_4_TURBO](#GPT-4-TURBO) | Type de modèle génératif GPT-4 Turbo. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String aiModelTypeName)](#fromName-java.lang.String) |  |
| [getName(int aiModelType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int aiModelType)](#toString-int) |  |
### CLAUDE_35_HAIKU {#CLAUDE-35-HAIKU}
```
public static int CLAUDE_35_HAIKU
```


Type de modèle génératif Claude 3.5 Haiku.

### CLAUDE_35_SONNET {#CLAUDE-35-SONNET}
```
public static int CLAUDE_35_SONNET
```


Type de modèle génératif Claude 3.5 Sonnet.

### CLAUDE_3_HAIKU {#CLAUDE-3-HAIKU}
```
public static int CLAUDE_3_HAIKU
```


Type de modèle génératif Claude 3 Haiku.

### CLAUDE_3_OPUS {#CLAUDE-3-OPUS}
```
public static int CLAUDE_3_OPUS
```


Type de modèle génératif Claude 3 Opus.

### CLAUDE_3_SONNET {#CLAUDE-3-SONNET}
```
public static int CLAUDE_3_SONNET
```


Type de modèle génératif Claude 3 Sonnet.

### GEMINI_FLASH_LATEST {#GEMINI-FLASH-LATEST}
```
public static int GEMINI_FLASH_LATEST
```


Type de modèle génératif Gemini Flash dernière version.

### GEMINI_PRO_LATEST {#GEMINI-PRO-LATEST}
```
public static int GEMINI_PRO_LATEST
```


Type de modèle génératif Gemini Pro dernière version.

### GPT_35_TURBO {#GPT-35-TURBO}
```
public static int GPT_35_TURBO
```


Type de modèle génératif GPT-3.5 Turbo.

### GPT_4_O {#GPT-4-O}
```
public static int GPT_4_O
```


Type de modèle génératif GPT-4o.

### GPT_4_O_MINI {#GPT-4-O-MINI}
```
public static int GPT_4_O_MINI
```


Type de modèle génératif GPT-4o mini.

### GPT_4_TURBO {#GPT-4-TURBO}
```
public static int GPT_4_TURBO
```


Type de modèle génératif GPT-4 Turbo.

### length {#length}
```
public static int length
```


### fromName(String aiModelTypeName) {#fromName-java.lang.String}
```
public static int fromName(String aiModelTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| aiModelTypeName | java.lang.String |  |

**Returns:**
int
### getName(int aiModelType) {#getName-int}
```
public static String getName(int aiModelType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| aiModelType | int |  |

**Returns:**
java.lang.String
