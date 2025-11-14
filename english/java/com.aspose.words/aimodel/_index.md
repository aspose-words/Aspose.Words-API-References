---
title: AiModel
linktitle: AiModel
second_title: Aspose.Words for Java
description: An abstract class representing the integration with various AI models within the Aspose.Words in Java.
type: docs
weight: 14
url: /java/com.aspose.words/aimodel/
---

**Inheritance:**
java.lang.Object
```
public abstract class AiModel
```

An abstract class representing the integration with various AI models within the Aspose.Words.

 **Examples:** 

Shows how to summarize text using OpenAI and Google models.

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
## Methods

| Method | Description |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Checks grammar of the provided document. |
| [create(int modelType)](#create-int) |  |
| [getTimeout()](#getTimeout) | Gets the number of milliseconds to wait before the request to AI model times out. |
| [getUrl()](#getUrl) | Gets a URL of the model. |
| [setTimeout(int value)](#setTimeout-int) | Sets the number of milliseconds to wait before the request to AI model times out. |
| [setUrl(String value)](#setUrl-java.lang.String) | Sets a URL of the model. |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Generates a summary of the specified document, with options to adjust the length of the summary. |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Generates summaries for an array of documents, with options to control the summary length and other settings. |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | Sets a specified API key to the model. |
### AiModel() {#AiModel}
```
public AiModel()
```


### checkGrammar(Document sourceDocument, CheckGrammarOptions options) {#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions}
```
public Document checkGrammar(Document sourceDocument, CheckGrammarOptions options)
```


Checks grammar of the provided document. This operation leverages the connected AI model for checking grammar of document.

 **Examples:** 

Shows how to check the grammar of a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | The document being checked for grammar. |
| options | [CheckGrammarOptions](../../com.aspose.words/checkgrammaroptions/) | Optional settings to control how grammar will be checked. |

**Returns:**
[Document](../../com.aspose.words/document/) - A new [Document](../../com.aspose.words/document/) with checked grammar.
### create(int modelType) {#create-int}
```
public static AiModel create(int modelType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| modelType | int |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
### getTimeout() {#getTimeout}
```
public int getTimeout()
```


Gets the number of milliseconds to wait before the request to AI model times out. The default value is 100,000 milliseconds (100 seconds).

 **Examples:** 

Shows how to change model default timeout.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value 100000ms.
 model.setTimeout(250000);
 
```

**Returns:**
int - The number of milliseconds to wait before the request to AI model times out.
### getUrl() {#getUrl}
```
public abstract String getUrl()
```


Gets a URL of the model. The default value is specific for the model.

 **Examples:** 

Shows how to change model default url.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value "https://api.openai.com/".
 model.setUrl("https://my.a.com/");
 
```

Shows how to use self-hosted AI model based on OpenAiModel.

```

 public void selfHostedModel() throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     String apiKey = System.getenv("API_KEY");
     // Use OpenAI generative language models.
     AiModel model = new CustomAiModel().withApiKey(apiKey);
     model.setUrl("https://my.a.com/");

     Document translatedDoc = model.translate(doc, Language.RUSSIAN);
     translatedDoc.save(getArtifactsDir() + "AI.SelfHostedModel.docx");
 }

 /// 
 /// Custom self-hosted AI model.
 /// 
 static class CustomAiModel extends OpenAiModel
 {
     /// 
     /// Gets model name.
     /// 
     protected  String getName() { return "my-model-24b"; }
 }
 
```

**Returns:**
java.lang.String - A URL of the model.
### setTimeout(int value) {#setTimeout-int}
```
public void setTimeout(int value)
```


Sets the number of milliseconds to wait before the request to AI model times out. The default value is 100,000 milliseconds (100 seconds).

 **Examples:** 

Shows how to change model default timeout.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value 100000ms.
 model.setTimeout(250000);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The number of milliseconds to wait before the request to AI model times out. |

### setUrl(String value) {#setUrl-java.lang.String}
```
public abstract void setUrl(String value)
```


Sets a URL of the model. The default value is specific for the model.

 **Examples:** 

Shows how to change model default url.

```

 String apiKey = System.getenv("API_KEY");
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);
 // Default value "https://api.openai.com/".
 model.setUrl("https://my.a.com/");
 
```

Shows how to use self-hosted AI model based on OpenAiModel.

```

 public void selfHostedModel() throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     String apiKey = System.getenv("API_KEY");
     // Use OpenAI generative language models.
     AiModel model = new CustomAiModel().withApiKey(apiKey);
     model.setUrl("https://my.a.com/");

     Document translatedDoc = model.translate(doc, Language.RUSSIAN);
     translatedDoc.save(getArtifactsDir() + "AI.SelfHostedModel.docx");
 }

 /// 
 /// Custom self-hosted AI model.
 /// 
 static class CustomAiModel extends OpenAiModel
 {
     /// 
     /// Gets model name.
     /// 
     protected  String getName() { return "my-model-24b"; }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A URL of the model. |

### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document sourceDocument, SummarizeOptions options)
```


Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected AI model for content processing.

 **Examples:** 

Shows how to summarize text using OpenAI and Google models.

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
| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | The document to be summarized. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Optional settings to control the summary length and other parameters. |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document[] sourceDocuments, SummarizeOptions options)
```


Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected AI model for processing each document in the array.

 **Examples:** 

Shows how to summarize text using OpenAI and Google models.

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
| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) | An array of documents to be summarized. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Optional settings to control the summary length and other parameters |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### translate(Document sourceDocument, int targetLanguage) {#translate-com.aspose.words.Document-int}
```
public abstract Document translate(Document sourceDocument, int targetLanguage)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| targetLanguage | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### withApiKey(String apiKey) {#withApiKey-java.lang.String}
```
public AiModel withApiKey(String apiKey)
```


Sets a specified API key to the model.

 **Examples:** 

Shows how to summarize text using OpenAI and Google models.

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
| Parameter | Type | Description |
| --- | --- | --- |
| apiKey | java.lang.String |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
