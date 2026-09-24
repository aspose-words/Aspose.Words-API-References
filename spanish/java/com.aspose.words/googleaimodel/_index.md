---
title: "GoogleAiModel"
linktitle: "GoogleAiModel"
second_title: "Aspose.Words para Java"
description: "Clase que representa la integración de Google AI Models Gemini dentro de Aspose.Words en Java."
type: docs
weight: 361
url: /es/java/com.aspose.words/googleaimodel/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.AiModel](../../com.aspose.words/aimodel/)
```
public class GoogleAiModel extends AiModel
```

Clase que representa la integración de los Modelos de IA de Google (Gemini) dentro de Aspose.Words.

 **Remarks:** 

Consulte https://ai.google.dev/gemini-api/docs/models para obtener detalles de los modelos Gemini.

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

Muestra cómo usar el modelo de IA de Google.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```
## Constructores

| Constructor | Descripción |
| --- | --- |
| [GoogleAiModel(String name)](#GoogleAiModel-java.lang.String) | Inicializa una nueva instancia de la clase [GoogleAiModel](../../com.aspose.words/googleaimodel/). |
| [GoogleAiModel(String name, String apiKey)](#GoogleAiModel-java.lang.String-java.lang.String) | Inicializa una nueva instancia de la clase [GoogleAiModel](../../com.aspose.words/googleaimodel/). |
## Métodos

| Método | Descripción |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Comprueba la gramática del documento proporcionado. |
| [create(int modelType)](#create-int) |  |
| [getTimeout()](#getTimeout) | Obtiene el número de milisegundos a esperar antes de que la solicitud al modelo de IA expire. |
| [getUrl()](#getUrl) | Obtiene una URL del modelo. |
| [setTimeout(int value)](#setTimeout-int) | Establece el número de milisegundos a esperar antes de que la solicitud al modelo de IA expire. |
| [setUrl(String value)](#setUrl-java.lang.String) | Establece una URL del modelo. |
| [summarize(Document doc)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document doc, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Resume el objeto [Document](../../com.aspose.words/document/) especificado. |
| [summarize(Document[] docs)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document[] docs, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Resume los objetos [Document](../../com.aspose.words/document/) especificados. |
| [translate(Document doc, int language)](#translate-com.aspose.words.Document-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | Establece una clave API especificada al modelo. |
### GoogleAiModel(String name) {#GoogleAiModel-java.lang.String}
```
public GoogleAiModel(String name)
```


Inicializa una nueva instancia de la clase [GoogleAiModel](../../com.aspose.words/googleaimodel/).

 **Examples:** 

Muestra cómo usar el modelo de IA de Google.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre del modelo. Por ejemplo, gemini-2.5-flash. |

### GoogleAiModel(String name, String apiKey) {#GoogleAiModel-java.lang.String-java.lang.String}
```
public GoogleAiModel(String name, String apiKey)
```


Inicializa una nueva instancia de la clase [GoogleAiModel](../../com.aspose.words/googleaimodel/).

 **Examples:** 

Muestra cómo usar el modelo de IA de Google.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre del modelo. Por ejemplo, gemini-2.5-flash. |
| apiKey | java.lang.String | La clave API para usar la API Gemini. Consulte https://ai.google.dev/gemini-api/docs/api-key para obtener detalles. |

### checkGrammar(Document sourceDocument, CheckGrammarOptions options) {#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions}
```
public Document checkGrammar(Document sourceDocument, CheckGrammarOptions options)
```


Comprueba la gramática del documento proporcionado. Esta operación utiliza el modelo de IA conectado para comprobar la gramática del documento.

 **Examples:** 

Muestra cómo comprobar la gramática de un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | El documento que se está comprobando para gramática. |
| options | [CheckGrammarOptions](../../com.aspose.words/checkgrammaroptions/) | Configuraciones opcionales para controlar cómo se comprobará la gramática. |

**Returns:**
[Document](../../com.aspose.words/document/) - A new [Document](../../com.aspose.words/document/) with checked grammar.
### create(int modelType) {#create-int}
```
public static AiModel create(int modelType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| modelType | int |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
### getTimeout() {#getTimeout}
```
public int getTimeout()
```


Obtiene el número de milisegundos a esperar antes de que la solicitud al modelo de IA expire. El valor predeterminado es 100.000 milisegundos (100 segundos).

 **Examples:** 

Muestra cómo cambiar el tiempo de espera predeterminado del modelo.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value 100000ms.
 model.setTimeout(250000);
 
```

**Returns:**
int - El número de milisegundos a esperar antes de que la solicitud al modelo de IA expire.
### getUrl() {#getUrl}
```
public String getUrl()
```


Obtiene una URL del modelo. El valor predeterminado es "https://generativelanguage.googleapis.com/v1beta/models/".

**Returns:**
java.lang.String - Una URL del modelo.
### setTimeout(int value) {#setTimeout-int}
```
public void setTimeout(int value)
```


Establece el número de milisegundos a esperar antes de que la solicitud al modelo de IA expire. El valor predeterminado es 100.000 milisegundos (100 segundos).

 **Examples:** 

Muestra cómo cambiar el tiempo de espera predeterminado del modelo.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value 100000ms.
 model.setTimeout(250000);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El número de milisegundos a esperar antes de que la solicitud al modelo de IA expire. |

### setUrl(String value) {#setUrl-java.lang.String}
```
public void setUrl(String value)
```


Establece una URL del modelo. El valor predeterminado es "https://generativelanguage.googleapis.com/v1beta/models/".

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | Una URL del modelo. |

### summarize(Document doc) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document doc)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document doc, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public Document summarize(Document doc, SummarizeOptions options)
```


Resume el objeto [Document](../../com.aspose.words/document/) especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| docs | [Document\[\]](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] docs, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public Document summarize(Document[] docs, SummarizeOptions options)
```


Resume los objetos [Document](../../com.aspose.words/document/) especificados.

**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |
| language | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### withApiKey(String apiKey) {#withApiKey-java.lang.String}
```
public AiModel withApiKey(String apiKey)
```


Establece una clave API especificada al modelo.

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| apiKey | java.lang.String |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
