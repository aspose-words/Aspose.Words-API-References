---
title: "GoogleAiModel"
linktitle: "GoogleAiModel"
second_title: "Aspose.Words für Java"
description: "Klasse, die die Integration von Google AI Models Gemini in Aspose.Words für Java darstellt."
type: docs
weight: 361
url: /de/java/com.aspose.words/googleaimodel/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.AiModel](../../com.aspose.words/aimodel/)
```
public class GoogleAiModel extends AiModel
```

Klasse, die die Integration von Google KI-Modellen (Gemini) in Aspose.Words darstellt.

 **Remarks:** 

Bitte beachten Sie https://ai.google.dev/gemini-api/docs/models für Details zu Gemini-Modellen.

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

Zeigt, wie man das Google AI‑Modell verwendet.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [GoogleAiModel(String name)](#GoogleAiModel-java.lang.String) | Initialisiert eine neue Instanz der Klasse [GoogleAiModel](../../com.aspose.words/googleaimodel/). |
| [GoogleAiModel(String name, String apiKey)](#GoogleAiModel-java.lang.String-java.lang.String) | Initialisiert eine neue Instanz der Klasse [GoogleAiModel](../../com.aspose.words/googleaimodel/). |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Überprüft die Grammatik des bereitgestellten Dokuments. |
| [create(int modelType)](#create-int) |  |
| [getTimeout()](#getTimeout) | Ermittelt die Anzahl der Millisekunden, die vor einem Timeout der Anfrage an das KI‑Modell gewartet werden. |
| [getUrl()](#getUrl) | Ermittelt die URL des Modells. |
| [setTimeout(int value)](#setTimeout-int) | Setzt die Anzahl der Millisekunden, die vor einem Timeout der Anfrage an das KI‑Modell gewartet werden. |
| [setUrl(String value)](#setUrl-java.lang.String) | Setzt die URL des Modells. |
| [summarize(Document doc)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document doc, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Fasst das angegebene [Document](../../com.aspose.words/document/)-Objekt zusammen. |
| [summarize(Document[] docs)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document[] docs, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Fasst die angegebenen [Document](../../com.aspose.words/document/)-Objekte zusammen. |
| [translate(Document doc, int language)](#translate-com.aspose.words.Document-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | Setzt einen angegebenen API‑Schlüssel für das Modell. |
### GoogleAiModel(String name) {#GoogleAiModel-java.lang.String}
```
public GoogleAiModel(String name)
```


Initialisiert eine neue Instanz der Klasse [GoogleAiModel](../../com.aspose.words/googleaimodel/).

 **Examples:** 

Zeigt, wie man das Google AI‑Modell verwendet.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name des Modells. Zum Beispiel gemini-2.5-flash. |

### GoogleAiModel(String name, String apiKey) {#GoogleAiModel-java.lang.String-java.lang.String}
```
public GoogleAiModel(String name, String apiKey)
```


Initialisiert eine neue Instanz der Klasse [GoogleAiModel](../../com.aspose.words/googleaimodel/).

 **Examples:** 

Zeigt, wie man das Google AI‑Modell verwendet.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name des Modells. Zum Beispiel gemini-2.5-flash. |
| apiKey | java.lang.String | Der API‑Schlüssel zur Verwendung der Gemini‑API. Bitte beachten Sie https://ai.google.dev/gemini-api/docs/api-key für Details. |

### checkGrammar(Document sourceDocument, CheckGrammarOptions options) {#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions}
```
public Document checkGrammar(Document sourceDocument, CheckGrammarOptions options)
```


Überprüft die Grammatik des bereitgestellten Dokuments. Dieser Vorgang nutzt das verbundene KI-Modell zur Grammatikprüfung des Dokuments.

 **Examples:** 

Zeigt, wie man die Grammatik eines Dokuments prüft.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use OpenAI generative language models.
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);

 CheckGrammarOptions grammarOptions = new CheckGrammarOptions();
 grammarOptions.setImproveStylistics(true);

 Document proofedDoc = model.checkGrammar(doc, grammarOptions);
 proofedDoc.save(getArtifactsDir() + "AI.AiGrammar.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Das Dokument, das auf Grammatik überprüft wird. |
| options | [CheckGrammarOptions](../../com.aspose.words/checkgrammaroptions/) | Optionale Einstellungen zur Steuerung, wie die Grammatik überprüft wird. |

**Returns:**
[Document](../../com.aspose.words/document/) - A new [Document](../../com.aspose.words/document/) with checked grammar.
### create(int modelType) {#create-int}
```
public static AiModel create(int modelType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| modelType | int |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
### getTimeout() {#getTimeout}
```
public int getTimeout()
```


Ermittelt die Anzahl der Millisekunden, die gewartet werden sollen, bevor die Anfrage an das KI‑Modell abläuft. Der Standardwert beträgt 100.000 Millisekunden (100 Sekunden).

 **Examples:** 

Zeigt, wie man den Standard‑Timeout des Modells ändert.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value 100000ms.
 model.setTimeout(250000);
 
```

**Returns:**
int – Die Anzahl der Millisekunden, die gewartet werden sollen, bevor die Anfrage an das KI‑Modell abläuft.
### getUrl() {#getUrl}
```
public String getUrl()
```


Liefert eine URL des Modells. Der Standardwert ist "https://generativelanguage.googleapis.com/v1beta/models/".

**Returns:**
java.lang.String – Eine URL des Modells.
### setTimeout(int value) {#setTimeout-int}
```
public void setTimeout(int value)
```


Legt die Anzahl der Millisekunden fest, die gewartet werden sollen, bevor die Anfrage an das KI‑Modell abläuft. Der Standardwert beträgt 100.000 Millisekunden (100 Sekunden).

 **Examples:** 

Zeigt, wie man den Standard‑Timeout des Modells ändert.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value 100000ms.
 model.setTimeout(250000);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Die Anzahl der Millisekunden, die gewartet werden sollen, bevor die Anfrage an das KI‑Modell abläuft. |

### setUrl(String value) {#setUrl-java.lang.String}
```
public void setUrl(String value)
```


Setzt eine URL des Modells. Der Standardwert ist "https://generativelanguage.googleapis.com/v1beta/models/".

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Eine URL des Modells. |

### summarize(Document doc) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document doc)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document doc, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public Document summarize(Document doc, SummarizeOptions options)
```


Fasst das angegebene [Document](../../com.aspose.words/document/)-Objekt zusammen.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] docs) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document[] docs)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| docs | [Document\[\]](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] docs, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public Document summarize(Document[] docs, SummarizeOptions options)
```


Fasst die angegebenen [Document](../../com.aspose.words/document/)-Objekte zusammen.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| docs | [Document\[\]](../../com.aspose.words/document/) |  |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### translate(Document doc, int language) {#translate-com.aspose.words.Document-int}
```
public Document translate(Document doc, int language)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |
| language | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### withApiKey(String apiKey) {#withApiKey-java.lang.String}
```
public AiModel withApiKey(String apiKey)
```


Setzt einen angegebenen API‑Schlüssel für das Modell.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| apiKey | java.lang.String |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
