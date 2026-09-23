---
title: "OpenAiModel"
linktitle: "OpenAiModel"
second_title: "Aspose.Words per Java"
description: "Classe che rappresenta l'integrazione dei modelli OpenAi all'interno di Aspose.Words in Java."
type: docs
weight: 505
url: /it/java/com.aspose.words/openaimodel/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.AiModel](../../com.aspose.words/aimodel/)
```
public class OpenAiModel extends AiModel
```

Classe che rappresenta l'integrazione dei modelli OpenAi all'interno di Aspose.Words.

 **Remarks:** 

Si prega di fare riferimento a https://platform.openai.com/docs/models per i dettagli dei modelli OpenAi.

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

Mostra come utilizzare un modello AI auto‑ospitato basato su OpenAiModel.

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
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [OpenAiModel(String name, String apiKey)](#OpenAiModel-java.lang.String-java.lang.String) | Inizializza una nuova istanza della classe [OpenAiModel](../../com.aspose.words/openaimodel/). |
| [OpenAiModel(String name)](#OpenAiModel-java.lang.String) | Inizializza una nuova istanza della classe [OpenAiModel](../../com.aspose.words/openaimodel/). |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Verifica la grammatica del documento fornito. |
| [create(int modelType)](#create-int) |  |
| [getTimeout()](#getTimeout) | Ottiene il numero di millisecondi da attendere prima che la richiesta al modello AI scada. |
| [getUrl()](#getUrl) | Ottiene un URL del modello. |
| [setTimeout(int value)](#setTimeout-int) | Imposta il numero di millisecondi da attendere prima che la richiesta al modello AI scada. |
| [setUrl(String value)](#setUrl-java.lang.String) | Imposta un URL del modello. |
| [summarize(Document sourceDocument)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Genera un riepilogo del documento specificato, con opzioni per regolare la lunghezza del riepilogo. |
| [summarize(Document[] sourceDocuments)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Genera riepiloghi per un array di documenti, con opzioni per controllare la lunghezza del riepilogo e altre impostazioni. |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | Imposta una chiave API specificata per il modello. |
| [withOrganization(String organizationId)](#withOrganization-java.lang.String) | Imposta un'Organizzazione specificata per il modello. |
| [withProject(String projectId)](#withProject-java.lang.String) | Imposta un Progetto specificato per il modello. |
### OpenAiModel(String name, String apiKey) {#OpenAiModel-java.lang.String-java.lang.String}
```
public OpenAiModel(String name, String apiKey)
```


Inizializza una nuova istanza della classe [OpenAiModel](../../com.aspose.words/openaimodel/).

 **Examples:** 

Mostra come creare un'istanza del modello OpenAI direttamente utilizzando una chiave API e il nome del modello.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome del modello. Per esempio, gpt-5.2-chat-latest. |
| apiKey | java.lang.String | La chiave API da utilizzare per l'API OpenAi. |

### OpenAiModel(String name) {#OpenAiModel-java.lang.String}
```
public OpenAiModel(String name)
```


Inizializza una nuova istanza della classe [OpenAiModel](../../com.aspose.words/openaimodel/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome del modello. Per esempio, gpt-5.2-chat-latest. |

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


Ottiene l'URL del modello. Il valore predefinito è "https://api.openai.com/".

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


Imposta l'URL del modello. Il valore predefinito è "https://api.openai.com/".

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Un URL del modello. |

### summarize(Document sourceDocument) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document sourceDocument)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public Document summarize(Document sourceDocument, SummarizeOptions options)
```


Genera un riepilogo del documento specificato, con opzioni per regolare la lunghezza del riepilogo. Questa operazione utilizza il modello AI connesso per l'elaborazione dei contenuti.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Il documento da riepilogare. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Impostazioni opzionali per controllare la lunghezza del riepilogo e altri parametri. |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] sourceDocuments) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document[] sourceDocuments)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public Document summarize(Document[] sourceDocuments, SummarizeOptions options)
```


Genera riepiloghi per un array di documenti, con opzioni per controllare la lunghezza del riepilogo e altre impostazioni. Questo metodo utilizza il modello AI connesso per l'elaborazione di ciascun documento nell'array.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) | Un array di documenti da riepilogare. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Impostazioni opzionali per controllare la lunghezza del riepilogo e altri parametri |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### translate(Document sourceDocument, int targetLanguage) {#translate-com.aspose.words.Document-int}
```
public Document translate(Document sourceDocument, int targetLanguage)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| targetLanguage | int |  |

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
### withOrganization(String organizationId) {#withOrganization-java.lang.String}
```
public OpenAiModel withOrganization(String organizationId)
```


Imposta un'Organizzazione specificata per il modello.

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
| organizationId | java.lang.String |  |

**Returns:**
[OpenAiModel](../../com.aspose.words/openaimodel/)
### withProject(String projectId) {#withProject-java.lang.String}
```
public OpenAiModel withProject(String projectId)
```


Imposta un Progetto specificato per il modello.

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
| projectId | java.lang.String |  |

**Returns:**
[OpenAiModel](../../com.aspose.words/openaimodel/)
