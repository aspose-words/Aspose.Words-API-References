---
title: "GoogleAiModel"
linktitle: "GoogleAiModel"
second_title: "Aspose.Words pour Java"
description: "Classe représentant l'intégration de Google AI Models Gemini dans Aspose.Words en Java."
type: docs
weight: 361
url: /fr/java/com.aspose.words/googleaimodel/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.AiModel](../../com.aspose.words/aimodel/)
```
public class GoogleAiModel extends AiModel
```

Classe représentant l'intégration des modèles d'IA Google (Gemini) dans Aspose.Words.

 **Remarks:** 

Veuillez vous référer à https://ai.google.dev/gemini-api/docs/models pour les détails des modèles Gemini.

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

Montre comment utiliser le modèle d'IA Google.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```
## Constructors

| Constructor | Description |
| --- | --- |
| [GoogleAiModel(String name)](#GoogleAiModel-java.lang.String) | Initialise une nouvelle instance de la classe [GoogleAiModel](../../com.aspose.words/googleaimodel/). |
| [GoogleAiModel(String name, String apiKey)](#GoogleAiModel-java.lang.String-java.lang.String) | Initialise une nouvelle instance de la classe [GoogleAiModel](../../com.aspose.words/googleaimodel/). |
## Méthodes

| Méthode | Description |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Vérifie la grammaire du document fourni. |
| [create(int modelType)](#create-int) |  |
| [getTimeout()](#getTimeout) | Obtient le nombre de millisecondes à attendre avant que la requête au modèle d'IA n'expire. |
| [getUrl()](#getUrl) | Obtient une URL du modèle. |
| [setTimeout(int value)](#setTimeout-int) | Définit le nombre de millisecondes à attendre avant que la requête au modèle d'IA n'expire. |
| [setUrl(String value)](#setUrl-java.lang.String) | Définit une URL du modèle. |
| [summarize(Document doc)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document doc, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Résume l'objet [Document](../../com.aspose.words/document/) spécifié. |
| [summarize(Document[] docs)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document[] docs, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Résume les objets [Document](../../com.aspose.words/document/) spécifiés. |
| [translate(Document doc, int language)](#translate-com.aspose.words.Document-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | Définit une clé API spécifiée pour le modèle. |
### GoogleAiModel(String name) {#GoogleAiModel-java.lang.String}
```
public GoogleAiModel(String name)
```


Initialise une nouvelle instance de la classe [GoogleAiModel](../../com.aspose.words/googleaimodel/).

 **Examples:** 

Montre comment utiliser le modèle d'IA Google.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom du modèle. Par exemple, gemini-2.5-flash. |

### GoogleAiModel(String name, String apiKey) {#GoogleAiModel-java.lang.String-java.lang.String}
```
public GoogleAiModel(String name, String apiKey)
```


Initialise une nouvelle instance de la classe [GoogleAiModel](../../com.aspose.words/googleaimodel/).

 **Examples:** 

Montre comment utiliser le modèle d'IA Google.

```

 String apiKey = System.getenv("API_KEY");
 GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

 Document doc = new Document(getMyDir() + "Big document.docx");
 SummarizeOptions summarizeOptions = new SummarizeOptions(); { summarizeOptions.setSummaryLength(SummaryLength.VERY_SHORT); }
 Document summary = model.summarize(doc, summarizeOptions);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom du modèle. Par exemple, gemini-2.5-flash. |
| apiKey | java.lang.String | La clé API pour utiliser l'API Gemini. Veuillez vous référer à https://ai.google.dev/gemini-api/docs/api-key pour plus de détails. |

### checkGrammar(Document sourceDocument, CheckGrammarOptions options) {#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions}
```
public Document checkGrammar(Document sourceDocument, CheckGrammarOptions options)
```


Vérifie la grammaire du document fourni. Cette opération utilise le modèle IA connecté pour vérifier la grammaire du document.

 **Examples:** 

Montre comment vérifier la grammaire d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Le document dont la grammaire est vérifiée. |
| options | [CheckGrammarOptions](../../com.aspose.words/checkgrammaroptions/) | Paramètres optionnels pour contrôler la façon dont la grammaire sera vérifiée. |

**Returns:**
[Document](../../com.aspose.words/document/) - A new [Document](../../com.aspose.words/document/) with checked grammar.
### create(int modelType) {#create-int}
```
public static AiModel create(int modelType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| modelType | int |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
### getTimeout() {#getTimeout}
```
public int getTimeout()
```


Obtient le nombre de millisecondes à attendre avant que la requête au modèle d'IA ne dépasse le délai d'attente. La valeur par défaut est de 100 000 millisecondes (100 secondes).

 **Examples:** 

Montre comment modifier le délai d'attente par défaut du modèle.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value 100000ms.
 model.setTimeout(250000);
 
```

**Returns:**
int - Le nombre de millisecondes à attendre avant que la requête au modèle d'IA ne dépasse le délai d'attente.
### getUrl() {#getUrl}
```
public String getUrl()
```


Obtient une URL du modèle. La valeur par défaut est "https://generativelanguage.googleapis.com/v1beta/models/".

**Returns:**
java.lang.String - Une URL du modèle.
### setTimeout(int value) {#setTimeout-int}
```
public void setTimeout(int value)
```


Définit le nombre de millisecondes à attendre avant que la requête au modèle d'IA ne dépasse le délai d'attente. La valeur par défaut est de 100 000 millisecondes (100 secondes).

 **Examples:** 

Montre comment modifier le délai d'attente par défaut du modèle.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value 100000ms.
 model.setTimeout(250000);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | Le nombre de millisecondes à attendre avant que la requête au modèle d'IA ne dépasse le délai d'attente. |

### setUrl(String value) {#setUrl-java.lang.String}
```
public void setUrl(String value)
```


Définit une URL du modèle. La valeur par défaut est "https://generativelanguage.googleapis.com/v1beta/models/".

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Une URL du modèle. |

### summarize(Document doc) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document doc)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document doc, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public Document summarize(Document doc, SummarizeOptions options)
```


Résume l'objet [Document](../../com.aspose.words/document/) spécifié.

**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| docs | [Document\[\]](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] docs, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public Document summarize(Document[] docs, SummarizeOptions options)
```


Résume les objets [Document](../../com.aspose.words/document/) spécifiés.

**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |
| language | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### withApiKey(String apiKey) {#withApiKey-java.lang.String}
```
public AiModel withApiKey(String apiKey)
```


Définit une clé API spécifiée pour le modèle.

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

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| apiKey | java.lang.String |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
