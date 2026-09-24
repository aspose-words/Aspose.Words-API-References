---
title: "OpenAiModel"
linktitle: "OpenAiModel"
second_title: "Aspose.Words para Java"
description: "Clase que representa la integración de modelos OpenAi dentro de Aspose.Words en Java."
type: docs
weight: 505
url: /es/java/com.aspose.words/openaimodel/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.AiModel](../../com.aspose.words/aimodel/)
```
public class OpenAiModel extends AiModel
```

Clase que representa la integración de modelos OpenAi dentro de Aspose.Words.

 **Remarks:** 

Consulte https://platform.openai.com/docs/models para obtener detalles de los modelos OpenAi.

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

Muestra cómo usar un modelo de IA autohospedado basado en OpenAiModel.

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
## Constructores

| Constructor | Descripción |
| --- | --- |
| [OpenAiModel(String name, String apiKey)](#OpenAiModel-java.lang.String-java.lang.String) | Inicializa una nueva instancia de la clase [OpenAiModel](../../com.aspose.words/openaimodel/). |
| [OpenAiModel(String name)](#OpenAiModel-java.lang.String) | Inicializa una nueva instancia de la clase [OpenAiModel](../../com.aspose.words/openaimodel/). |
## Métodos

| Método | Descripción |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Comprueba la gramática del documento proporcionado. |
| [create(int modelType)](#create-int) |  |
| [getTimeout()](#getTimeout) | Obtiene el número de milisegundos a esperar antes de que la solicitud al modelo de IA expire. |
| [getUrl()](#getUrl) | Obtiene una URL del modelo. |
| [setTimeout(int value)](#setTimeout-int) | Establece el número de milisegundos a esperar antes de que la solicitud al modelo de IA expire. |
| [setUrl(String value)](#setUrl-java.lang.String) | Establece una URL del modelo. |
| [summarize(Document sourceDocument)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Genera un resumen del documento especificado, con opciones para ajustar la longitud del resumen. |
| [summarize(Document[] sourceDocuments)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Genera resúmenes para una matriz de documentos, con opciones para controlar la longitud del resumen y otras configuraciones. |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | Establece una clave API especificada al modelo. |
| [withOrganization(String organizationId)](#withOrganization-java.lang.String) | Establece una Organización especificada al modelo. |
| [withProject(String projectId)](#withProject-java.lang.String) | Establece un Proyecto especificado al modelo. |
### OpenAiModel(String name, String apiKey) {#OpenAiModel-java.lang.String-java.lang.String}
```
public OpenAiModel(String name, String apiKey)
```


Inicializa una nueva instancia de la clase [OpenAiModel](../../com.aspose.words/openaimodel/).

 **Examples:** 

Muestra cómo crear una instancia de modelo OpenAI directamente usando una clave API y el nombre del modelo.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre del modelo. Por ejemplo, gpt-5.2-chat-latest. |
| apiKey | java.lang.String | La clave API para usar la API de OpenAi. |

### OpenAiModel(String name) {#OpenAiModel-java.lang.String}
```
public OpenAiModel(String name)
```


Inicializa una nueva instancia de la clase [OpenAiModel](../../com.aspose.words/openaimodel/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre del modelo. Por ejemplo, gpt-5.2-chat-latest. |

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


Obtiene una URL del modelo. El valor predeterminado es "https://api.openai.com/".

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


Establece una URL del modelo. El valor predeterminado es "https://api.openai.com/".

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | Una URL del modelo. |

### summarize(Document sourceDocument) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document sourceDocument)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public Document summarize(Document sourceDocument, SummarizeOptions options)
```


Genera un resumen del documento especificado, con opciones para ajustar la longitud del resumen. Esta operación utiliza el modelo de IA conectado para el procesamiento de contenido.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | El documento a resumir. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Configuraciones opcionales para controlar la longitud del resumen y otros parámetros. |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] sourceDocuments) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document[] sourceDocuments)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public Document summarize(Document[] sourceDocuments, SummarizeOptions options)
```


Genera resúmenes para una matriz de documentos, con opciones para controlar la longitud del resumen y otras configuraciones. Este método utiliza el modelo de IA conectado para procesar cada documento en la matriz.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) | Una matriz de documentos a resumir. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Configuraciones opcionales para controlar la longitud del resumen y otros parámetros |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### translate(Document sourceDocument, int targetLanguage) {#translate-com.aspose.words.Document-int}
```
public Document translate(Document sourceDocument, int targetLanguage)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| targetLanguage | int |  |

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
### withOrganization(String organizationId) {#withOrganization-java.lang.String}
```
public OpenAiModel withOrganization(String organizationId)
```


Establece una Organización especificada al modelo.

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
| organizationId | java.lang.String |  |

**Returns:**
[OpenAiModel](../../com.aspose.words/openaimodel/)
### withProject(String projectId) {#withProject-java.lang.String}
```
public OpenAiModel withProject(String projectId)
```


Establece un Proyecto especificado al modelo.

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
| projectId | java.lang.String |  |

**Returns:**
[OpenAiModel](../../com.aspose.words/openaimodel/)
