---
title: "AiModel"
linktitle: "AiModel"
second_title: "Aspose.Words pour Java"
description: "Une classe abstraite représentant l'intégration avec divers modèles d'IA au sein d'Aspose.Words en Java."
type: docs
weight: 14
url: /fr/java/com.aspose.words/aimodel/
---

**Inheritance:**
java.lang.Object
```
public abstract class AiModel
```

Une classe abstraite représentant l'intégration avec divers modèles d'IA au sein d'Aspose.Words.

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
## Constructors

| Constructor | Description |
| --- | --- |
| [AiModel()](#AiModel) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Vérifie la grammaire du document fourni. |
| [create(int modelType)](#create-int) |  |
| [getTimeout()](#getTimeout) | Obtient le nombre de millisecondes à attendre avant que la requête au modèle d'IA n'expire. |
| [getUrl()](#getUrl) | Obtient une URL du modèle. |
| [setTimeout(int value)](#setTimeout-int) | Définit le nombre de millisecondes à attendre avant que la requête au modèle d'IA n'expire. |
| [setUrl(String value)](#setUrl-java.lang.String) | Définit une URL du modèle. |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Génère un résumé du document spécifié, avec des options pour ajuster la longueur du résumé. |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Génère des résumés pour un tableau de documents, avec des options pour contrôler la longueur du résumé et d'autres paramètres. |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | Définit une clé API spécifiée pour le modèle. |
### AiModel() {#AiModel}
```
public AiModel()
```


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
public abstract String getUrl()
```


Obtient une URL du modèle. La valeur par défaut est spécifique au modèle.

 **Examples:** 

Montre comment utiliser un modèle d'IA auto‑hébergé basé sur OpenAiModel.

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

Montre comment modifier l'URL par défaut du modèle.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value "https://api.openai.com/".
 model.setUrl("https://my.a.com/");
 
```

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
public abstract void setUrl(String value)
```


Définit une URL du modèle. La valeur par défaut est spécifique au modèle.

 **Examples:** 

Montre comment utiliser un modèle d'IA auto‑hébergé basé sur OpenAiModel.

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

Montre comment modifier l'URL par défaut du modèle.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value "https://api.openai.com/".
 model.setUrl("https://my.a.com/");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Une URL du modèle. |

### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document sourceDocument, SummarizeOptions options)
```


Génère un résumé du document spécifié, avec des options pour ajuster la longueur du résumé. Cette opération utilise le modèle IA connecté pour le traitement du contenu.

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
| sourceDocument | [Document](../../com.aspose.words/document/) | Le document à résumer. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Paramètres optionnels pour contrôler la longueur du résumé et d'autres paramètres. |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document[] sourceDocuments, SummarizeOptions options)
```


Génère des résumés pour un tableau de documents, avec des options pour contrôler la longueur du résumé et d'autres paramètres. Cette méthode utilise le modèle IA connecté pour le traitement de chaque document du tableau.

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
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) | Un tableau de documents à résumer. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Paramètres optionnels pour contrôler la longueur du résumé et d'autres paramètres |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### translate(Document sourceDocument, int targetLanguage) {#translate-com.aspose.words.Document-int}
```
public abstract Document translate(Document sourceDocument, int targetLanguage)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| targetLanguage | int |  |

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
