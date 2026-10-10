---
title: "OpenAiModel"
linktitle: "OpenAiModel"
second_title: "Aspose.Words für Java"
description: "Klasse, die die Integration von OpenAi-Modellen in Aspose.Words in Java darstellt."
type: docs
weight: 505
url: /de/java/com.aspose.words/openaimodel/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.AiModel](../../com.aspose.words/aimodel/)
```
public class OpenAiModel extends AiModel
```

Klasse, die die Integration von OpenAi‑Modellen in Aspose.Words darstellt.

 **Remarks:** 

Bitte beachten Sie https://platform.openai.com/docs/models für Details zu OpenAi-Modellen.

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

Zeigt, wie man ein selbstgehostetes KI‑Modell basierend auf OpenAiModel verwendet.

```

 public void selfHostedModel() throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     String apiKey = System.getenv("API_KEY");
     // Use OpenAI generative language models.
     AiModel model = new CustomAiModel("my-model-24b", "https://my.a.com/").withApiKey(apiKey);

     Document translatedDoc = model.translate(doc, Language.RUSSIAN);
     translatedDoc.save(getArtifactsDir() + "AI.SelfHostedModel.docx");
 }

 /// 
 /// Custom self-hosted AI model.
 /// 
 static class CustomAiModel extends OpenAiModel
 {
     CustomAiModel(String name, String url)
     {
         super(name);

         mUrl = url;
     }

     public String getUrl() { return mUrl; }

     private String mUrl;
 }
 
```
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [OpenAiModel(String name, String apiKey)](#OpenAiModel-java.lang.String-java.lang.String) | Initialisiert eine neue Instanz der Klasse [OpenAiModel](../../com.aspose.words/openaimodel/). |
| [OpenAiModel(String name)](#OpenAiModel-java.lang.String) | Initialisiert eine neue Instanz der Klasse [OpenAiModel](../../com.aspose.words/openaimodel/). |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Überprüft die Grammatik des bereitgestellten Dokuments. |
| [create(int modelType)](#create-int) |  |
| [getTimeout()](#getTimeout) | Ermittelt die Anzahl der Millisekunden, die vor einem Timeout der Anfrage an das KI‑Modell gewartet werden. |
| [getUrl()](#getUrl) | Ermittelt die URL des Modells. |
| [setTimeout(int value)](#setTimeout-int) | Setzt die Anzahl der Millisekunden, die vor einem Timeout der Anfrage an das KI‑Modell gewartet werden. |
| [setUrl(String value)](#setUrl-java.lang.String) | Setzt die URL des Modells. |
| [summarize(Document sourceDocument)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Erstellt eine Zusammenfassung des angegebenen Dokuments, mit Optionen zur Anpassung der Länge der Zusammenfassung. |
| [summarize(Document[] sourceDocuments)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Erstellt Zusammenfassungen für ein Array von Dokumenten, mit Optionen zur Steuerung der Zusammenfassungslänge und anderer Einstellungen. |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | Setzt einen angegebenen API‑Schlüssel für das Modell. |
| [withOrganization(String organizationId)](#withOrganization-java.lang.String) | Legt eine angegebene Organisation für das Modell fest. |
| [withProject(String projectId)](#withProject-java.lang.String) | Legt ein angegebenes Projekt für das Modell fest. |
### OpenAiModel(String name, String apiKey) {#OpenAiModel-java.lang.String-java.lang.String}
```
public OpenAiModel(String name, String apiKey)
```


Initialisiert eine neue Instanz der Klasse [OpenAiModel](../../com.aspose.words/openaimodel/).

 **Examples:** 

Zeigt, wie man eine OpenAI‑Modelinstanz direkt mit einem API‑Schlüssel und Modellnamen erstellt.

```

 String apiKey = System.getenv("API_KEY");
 // Create an OpenAI model instance using the constructor with model name and API key.
 OpenAiModel model = new OpenAiModel("gpt-4o-mini", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 // Summarize the document using the OpenAI model with short summary length.
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);

 summary.save(getArtifactsDir() + "OpenAiModel.OpenAiModelConstructor.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name des Modells. Zum Beispiel gpt-5.2-chat-latest. |
| apiKey | java.lang.String | Der API‑Schlüssel zur Verwendung der OpenAi‑API. |

### OpenAiModel(String name) {#OpenAiModel-java.lang.String}
```
public OpenAiModel(String name)
```


Initialisiert eine neue Instanz der Klasse [OpenAiModel](../../com.aspose.words/openaimodel/).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name des Modells. Zum Beispiel gpt-5.2-chat-latest. |

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


Ermittelt eine URL des Modells. Der Standardwert ist "https://api.openai.com/".

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


Legt eine URL des Modells fest. Der Standardwert ist "https://api.openai.com/".

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Eine URL des Modells. |

### summarize(Document sourceDocument) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document sourceDocument)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public Document summarize(Document sourceDocument, SummarizeOptions options)
```


Erstellt eine Zusammenfassung des angegebenen Dokuments, mit Optionen zur Anpassung der Länge der Zusammenfassung. Dieser Vorgang nutzt das verbundene KI-Modell zur Inhaltsverarbeitung.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Das zu zusammenfassende Dokument. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Optionale Einstellungen zur Steuerung der Zusammenfassungslänge und anderer Parameter. |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] sourceDocuments) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document[] sourceDocuments)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public Document summarize(Document[] sourceDocuments, SummarizeOptions options)
```


Erstellt Zusammenfassungen für ein Array von Dokumenten, mit Optionen zur Steuerung der Zusammenfassungslänge und anderer Einstellungen. Diese Methode nutzt das verbundene KI-Modell zur Verarbeitung jedes Dokuments im Array.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) | Ein Array von Dokumenten, die zusammengefasst werden sollen. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Optionale Einstellungen zur Steuerung der Zusammenfassungslänge und anderer Parameter |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### translate(Document sourceDocument, int targetLanguage) {#translate-com.aspose.words.Document-int}
```
public Document translate(Document sourceDocument, int targetLanguage)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| targetLanguage | int |  |

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
### withOrganization(String organizationId) {#withOrganization-java.lang.String}
```
public OpenAiModel withOrganization(String organizationId)
```


Legt eine angegebene Organisation für das Modell fest.

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
| organizationId | java.lang.String |  |

**Returns:**
[OpenAiModel](../../com.aspose.words/openaimodel/)
### withProject(String projectId) {#withProject-java.lang.String}
```
public OpenAiModel withProject(String projectId)
```


Legt ein angegebenes Projekt für das Modell fest.

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
| projectId | java.lang.String |  |

**Returns:**
[OpenAiModel](../../com.aspose.words/openaimodel/)
