---
title: "GoogleAiModel"
linktitle: "GoogleAiModel"
second_title: "Aspose.Words per Java"
description: "Classe che rappresenta l'integrazione di Google AI Models Gemini all'interno di Aspose.Words in Java."
type: docs
weight: 361
url: /it/java/com.aspose.words/googleaimodel/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.AiModel](../../com.aspose.words/aimodel/)
```
public class GoogleAiModel extends AiModel
```

Classe che rappresenta l'integrazione dei modelli AI di Google (Gemini) all'interno di Aspose.Words.

 **Remarks:** 

Fare riferimento a https://ai.google.dev/gemini-api/docs/models per i dettagli dei modelli Gemini.

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

Mostra come utilizzare il modello AI di Google.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [GoogleAiModel(String name)](#GoogleAiModel-java.lang.String) | Inizializza una nuova istanza della classe [GoogleAiModel](../../com.aspose.words/googleaimodel/). |
| [GoogleAiModel(String name, String apiKey)](#GoogleAiModel-java.lang.String-java.lang.String) | Inizializza una nuova istanza della classe [GoogleAiModel](../../com.aspose.words/googleaimodel/). |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Verifica la grammatica del documento fornito. |
| [create(int modelType)](#create-int) |  |
| [getTimeout()](#getTimeout) | Ottiene il numero di millisecondi da attendere prima che la richiesta al modello AI scada. |
| [getUrl()](#getUrl) | Ottiene un URL del modello. |
| [setTimeout(int value)](#setTimeout-int) | Imposta il numero di millisecondi da attendere prima che la richiesta al modello AI scada. |
| [setUrl(String value)](#setUrl-java.lang.String) | Imposta un URL del modello. |
| [summarize(Document doc)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document doc, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Riassume l'oggetto [Document](../../com.aspose.words/document/) specificato. |
| [summarize(Document[] docs)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document[] docs, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Riassume gli oggetti [Document](../../com.aspose.words/document/) specificati. |
| [translate(Document doc, int language)](#translate-com.aspose.words.Document-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | Imposta una chiave API specificata per il modello. |
### GoogleAiModel(String name) {#GoogleAiModel-java.lang.String}
```
public GoogleAiModel(String name)
```


Inizializza una nuova istanza della classe [GoogleAiModel](../../com.aspose.words/googleaimodel/).

 **Examples:** 

Mostra come utilizzare il modello AI di Google.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome del modello. Per esempio, gemini-2.5-flash. |

### GoogleAiModel(String name, String apiKey) {#GoogleAiModel-java.lang.String-java.lang.String}
```
public GoogleAiModel(String name, String apiKey)
```


Inizializza una nuova istanza della classe [GoogleAiModel](../../com.aspose.words/googleaimodel/).

 **Examples:** 

Mostra come utilizzare il modello AI di Google.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome del modello. Per esempio, gemini-2.5-flash. |
| apiKey | java.lang.String | La chiave API per utilizzare l'API Gemini. Fare riferimento a https://ai.google.dev/gemini-api/docs/api-key per i dettagli. |

### checkGrammar(Document sourceDocument, CheckGrammarOptions options) {#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions}
```
public Document checkGrammar(Document sourceDocument, CheckGrammarOptions options)
```


Verifica la grammatica del documento fornito. Questa operazione utilizza il modello AI connesso per la verifica della grammatica del documento.

 **Examples:** 

Mostra come controllare la grammatica di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Il documento in fase di verifica grammaticale. |
| options | [CheckGrammarOptions](../../com.aspose.words/checkgrammaroptions/) | Impostazioni opzionali per controllare come verrà verificata la grammatica. |

**Returns:**
[Document](../../com.aspose.words/document/) - A new [Document](../../com.aspose.words/document/) with checked grammar.
### create(int modelType) {#create-int}
```
public static AiModel create(int modelType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| modelType | int |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
### getTimeout() {#getTimeout}
```
public int getTimeout()
```


Ottiene il numero di millisecondi da attendere prima che la richiesta al modello AI scada. Il valore predefinito è 100.000 millisecondi (100 secondi).

 **Examples:** 

Mostra come modificare il timeout predefinito del modello.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value 100000ms.
 model.setTimeout(250000);
 
```

**Returns:**
int - Il numero di millisecondi da attendere prima che la richiesta al modello AI scada.
### getUrl() {#getUrl}
```
public String getUrl()
```


Ottiene un URL del modello. Il valore predefinito è "https://generativelanguage.googleapis.com/v1beta/models/".

**Returns:**
java.lang.String - Un URL del modello.
### setTimeout(int value) {#setTimeout-int}
```
public void setTimeout(int value)
```


Imposta il numero di millisecondi da attendere prima che la richiesta al modello AI scada. Il valore predefinito è 100.000 millisecondi (100 secondi).

 **Examples:** 

Mostra come modificare il timeout predefinito del modello.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value 100000ms.
 model.setTimeout(250000);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il numero di millisecondi da attendere prima che la richiesta al modello AI scada. |

### setUrl(String value) {#setUrl-java.lang.String}
```
public void setUrl(String value)
```


Imposta un URL del modello. Il valore predefinito è "https://generativelanguage.googleapis.com/v1beta/models/".

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Un URL del modello. |

### summarize(Document doc) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document doc)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document doc, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public Document summarize(Document doc, SummarizeOptions options)
```


Riassume l'oggetto [Document](../../com.aspose.words/document/) specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| docs | [Document\[\]](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] docs, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public Document summarize(Document[] docs, SummarizeOptions options)
```


Riassume gli oggetti [Document](../../com.aspose.words/document/) specificati.

**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |
| language | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### withApiKey(String apiKey) {#withApiKey-java.lang.String}
```
public AiModel withApiKey(String apiKey)
```


Imposta una chiave API specificata per il modello.

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

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| apiKey | java.lang.String |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
