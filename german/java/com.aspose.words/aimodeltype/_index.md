---
title: "AiModelType"
linktitle: "AiModelType"
second_title: "Aspose.Words für Java"
description: "Stellt die Typen von AiModel dar, die in den Dokumentverarbeitungs-Workflow in Java integriert werden können."
type: docs
weight: 15
url: /de/java/com.aspose.words/aimodeltype/
---

**Inheritance:**
java.lang.Object
```
public class AiModelType
```

Stellt die Typen von [AiModel](../../com.aspose.words/aimodel/) dar, die in den Dokumentverarbeitungs-Workflow integriert werden können.

 **Remarks:** 

Diese Aufzählung wird verwendet, um festzulegen, welches große Sprachmodell (LLM) für Aufgaben wie Zusammenfassung, Übersetzung und Inhaltserstellung genutzt werden soll.

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
| [CLAUDE_35_HAIKU](#CLAUDE-35-HAIKU) | Claude 3.5 Haiku-generativer Modultyp. |
| [CLAUDE_35_SONNET](#CLAUDE-35-SONNET) | Claude 3.5 Sonnet-generativer Modultyp. |
| [CLAUDE_3_HAIKU](#CLAUDE-3-HAIKU) | Claude 3 Haiku-generativer Modultyp. |
| [CLAUDE_3_OPUS](#CLAUDE-3-OPUS) | Claude 3 Opus-generativer Modultyp. |
| [CLAUDE_3_SONNET](#CLAUDE-3-SONNET) | Claude 3 Sonnet-generativer Modultyp. |
| [GEMINI_FLASH_LATEST](#GEMINI-FLASH-LATEST) | Gemini Flash-generativer Modultyp der neuesten Version. |
| [GEMINI_PRO_LATEST](#GEMINI-PRO-LATEST) | Gemini Pro-generativer Modultyp der neuesten Version. |
| [GPT_35_TURBO](#GPT-35-TURBO) | GPT-3.5 Turbo-generativer Modultyp. |
| [GPT_4_O](#GPT-4-O) | GPT-4o-generativer Modultyp. |
| [GPT_4_O_MINI](#GPT-4-O-MINI) | GPT-4o mini-generativer Modultyp. |
| [GPT_4_TURBO](#GPT-4-TURBO) | GPT-4 Turbo generativer Modelltyp. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String aiModelTypeName)](#fromName-java.lang.String) |  |
| [getName(int aiModelType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int aiModelType)](#toString-int) |  |
### CLAUDE_35_HAIKU {#CLAUDE-35-HAIKU}
```
public static int CLAUDE_35_HAIKU
```


Claude 3.5 Haiku-generativer Modultyp.

### CLAUDE_35_SONNET {#CLAUDE-35-SONNET}
```
public static int CLAUDE_35_SONNET
```


Claude 3.5 Sonnet-generativer Modultyp.

### CLAUDE_3_HAIKU {#CLAUDE-3-HAIKU}
```
public static int CLAUDE_3_HAIKU
```


Claude 3 Haiku-generativer Modultyp.

### CLAUDE_3_OPUS {#CLAUDE-3-OPUS}
```
public static int CLAUDE_3_OPUS
```


Claude 3 Opus-generativer Modultyp.

### CLAUDE_3_SONNET {#CLAUDE-3-SONNET}
```
public static int CLAUDE_3_SONNET
```


Claude 3 Sonnet-generativer Modultyp.

### GEMINI_FLASH_LATEST {#GEMINI-FLASH-LATEST}
```
public static int GEMINI_FLASH_LATEST
```


Gemini Flash-generativer Modultyp der neuesten Version.

### GEMINI_PRO_LATEST {#GEMINI-PRO-LATEST}
```
public static int GEMINI_PRO_LATEST
```


Gemini Pro-generativer Modultyp der neuesten Version.

### GPT_35_TURBO {#GPT-35-TURBO}
```
public static int GPT_35_TURBO
```


GPT-3.5 Turbo-generativer Modultyp.

### GPT_4_O {#GPT-4-O}
```
public static int GPT_4_O
```


GPT-4o-generativer Modultyp.

### GPT_4_O_MINI {#GPT-4-O-MINI}
```
public static int GPT_4_O_MINI
```


GPT-4o mini-generativer Modultyp.

### GPT_4_TURBO {#GPT-4-TURBO}
```
public static int GPT_4_TURBO
```


GPT-4 Turbo generativer Modelltyp.

### length {#length}
```
public static int length
```


### fromName(String aiModelTypeName) {#fromName-java.lang.String}
```
public static int fromName(String aiModelTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| aiModelTypeName | java.lang.String |  |

**Returns:**
int
### getName(int aiModelType) {#getName-int}
```
public static String getName(int aiModelType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| aiModelType | int |  |

**Returns:**
java.lang.String
