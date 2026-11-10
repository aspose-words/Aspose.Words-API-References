---
title: AsposeLlmModel
linktitle: AsposeLlmModel
second_title: Aspose.Words for Java
description: Provides AI-powered document processing backed by Aspose.LLM - an on-premise LLM inference engine that runs entirely inside the current process so document content never leaves the machine in Java.
type: docs
weight: 20
url: /java/com.aspose.words/asposellmmodel/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.AiModel](../../com.aspose.words/aimodel/)
```
public class AsposeLlmModel extends AiModel
```

Provides AI-powered document processing backed by Aspose.LLM - an on-premise LLM inference engine that runs entirely inside the current process, so document content never leaves the machine.

 **Remarks:** 

Unlike [OpenAiModel](../../com.aspose.words/openaimodel/) / [GoogleAiModel](../../com.aspose.words/googleaimodel/) / the Anthropic models, this class never performs an HTTP request.

Aspose.LLM is not a dependency of Aspose.Words. To use this class, install the Aspose.LLM package (version 26.6.0 or higher) into your project, so that Aspose.LLM.dll is placed next to Aspose.Words.dll. If it cannot be loaded, the first call to the model throws java.lang.IllegalStateException.

Aspose.LLM has its own license, separate from the Aspose.Words license. You should set it directly, the same way as for any other Aspose product, for example:

```

 new Aspose.LLM.License().SetLicense("Aspose.Total.lic");
 
```

This class does not manage that license itself.

The native runtime and the model weights are downloaded by Aspose.LLM on the first request.

Every request is sent in its own chat session, so requests do not affect each other.
## Constructors

| Constructor | Description |
| --- | --- |
| [AsposeLlmModel(String presetName)](#AsposeLlmModel-java.lang.String) | Initializes a new instance of the [AsposeLlmModel](../../com.aspose.words/asposellmmodel/) class for a specified Aspose.LLM preset. |
## Methods

| Method | Description |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Checks grammar of the provided document. |
| [create(int modelType)](#create-int) |  |
| [dispose()](#dispose) | Releases the underlying Aspose.LLM model and its native resources. |
| [getTimeout()](#getTimeout) | Gets the number of milliseconds to wait before the request to AI model times out. |
| [getUrl()](#getUrl) | Not used: [AsposeLlmModel](../../com.aspose.words/asposellmmodel/) runs inference in-process against a local model, so there is no remote endpoint to address. |
| [setTimeout(int value)](#setTimeout-int) | Sets the number of milliseconds to wait before the request to AI model times out. |
| [setUrl(String value)](#setUrl-java.lang.String) | Not used: [AsposeLlmModel](../../com.aspose.words/asposellmmodel/) runs inference in-process against a local model, so there is no remote endpoint to address. |
| [summarize(Document sourceDocument)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Generates a summary of the specified document, with options to adjust the length of the summary. |
| [summarize(Document[] sourceDocuments)](#summarize-com.aspose.words.Document) |  |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Generates a summary for an array of documents, with options to adjust the length of the summary. |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | Sets a specified API key to the model. |
### AsposeLlmModel(String presetName) {#AsposeLlmModel-java.lang.String}
```
public AsposeLlmModel(String presetName)
```


Initializes a new instance of the [AsposeLlmModel](../../com.aspose.words/asposellmmodel/) class for a specified Aspose.LLM preset.

 **Examples:** 

Shows how to summarize documents with a local model, so the content never leaves the machine.

```

 // Aspose.LLM is a separate package with its own license, for example:
 // new Aspose.LLM.License().SetLicense("Aspose.Total.lic");
 Document firstDoc = new Document(getMyDir() + "Big document.docx");
 Document secondDoc = new Document(getMyDir() + "Document.docx");

 // Disposing the model releases the local model and its native resources.
 AsposeLlmModel model = new AsposeLlmModel("Qwen25_3BPresetCpu");
 SummarizeOptions summarizeOptions = new SummarizeOptions();

 summarizeOptions.setSummaryLength(SummaryLength.SHORT);
 Document summary = model.summarize(firstDoc, summarizeOptions);
 summary.save(getArtifactsDir() + "AI.AsposeLlmSummarize.One.docx");

 summarizeOptions.setSummaryLength(SummaryLength.MEDIUM);
 Document combinedSummary = model.summarize(new Document[] { firstDoc, secondDoc }, summarizeOptions);
 combinedSummary.save(getArtifactsDir() + "AI.AsposeLlmSummarize.Multiple.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| presetName | java.lang.String | The name of the Aspose.LLM preset class that selects the local model family and its runtime, for example "Qwen25Preset". Nothing is loaded or downloaded when this constructor runs. |

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
### dispose() {#dispose}
```
public void dispose()
```


Releases the underlying Aspose.LLM model and its native resources.

 **Examples:** 

Shows how to summarize documents with a local model, so the content never leaves the machine.

```

 // Aspose.LLM is a separate package with its own license, for example:
 // new Aspose.LLM.License().SetLicense("Aspose.Total.lic");
 Document firstDoc = new Document(getMyDir() + "Big document.docx");
 Document secondDoc = new Document(getMyDir() + "Document.docx");

 // Disposing the model releases the local model and its native resources.
 AsposeLlmModel model = new AsposeLlmModel("Qwen25_3BPresetCpu");
 SummarizeOptions summarizeOptions = new SummarizeOptions();

 summarizeOptions.setSummaryLength(SummaryLength.SHORT);
 Document summary = model.summarize(firstDoc, summarizeOptions);
 summary.save(getArtifactsDir() + "AI.AsposeLlmSummarize.One.docx");

 summarizeOptions.setSummaryLength(SummaryLength.MEDIUM);
 Document combinedSummary = model.summarize(new Document[] { firstDoc, secondDoc }, summarizeOptions);
 combinedSummary.save(getArtifactsDir() + "AI.AsposeLlmSummarize.Multiple.docx");
 
```

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
public String getUrl()
```


Not used: [AsposeLlmModel](../../com.aspose.words/asposellmmodel/) runs inference in-process against a local model, so there is no remote endpoint to address. Present only to satisfy the [AiModel](../../com.aspose.words/aimodel/) contract.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
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
public void setUrl(String value)
```


Not used: [AsposeLlmModel](../../com.aspose.words/asposellmmodel/) runs inference in-process against a local model, so there is no remote endpoint to address. Present only to satisfy the [AiModel](../../com.aspose.words/aimodel/) contract.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### summarize(Document sourceDocument) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document sourceDocument)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public Document summarize(Document sourceDocument, SummarizeOptions options)
```


Generates a summary of the specified document, with options to adjust the length of the summary.

 **Examples:** 

Shows how to summarize documents with a local model, so the content never leaves the machine.

```

 // Aspose.LLM is a separate package with its own license, for example:
 // new Aspose.LLM.License().SetLicense("Aspose.Total.lic");
 Document firstDoc = new Document(getMyDir() + "Big document.docx");
 Document secondDoc = new Document(getMyDir() + "Document.docx");

 // Disposing the model releases the local model and its native resources.
 AsposeLlmModel model = new AsposeLlmModel("Qwen25_3BPresetCpu");
 SummarizeOptions summarizeOptions = new SummarizeOptions();

 summarizeOptions.setSummaryLength(SummaryLength.SHORT);
 Document summary = model.summarize(firstDoc, summarizeOptions);
 summary.save(getArtifactsDir() + "AI.AsposeLlmSummarize.One.docx");

 summarizeOptions.setSummaryLength(SummaryLength.MEDIUM);
 Document combinedSummary = model.summarize(new Document[] { firstDoc, secondDoc }, summarizeOptions);
 combinedSummary.save(getArtifactsDir() + "AI.AsposeLlmSummarize.Multiple.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] sourceDocuments) {#summarize-com.aspose.words.Document}
```
public Document summarize(Document[] sourceDocuments)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public Document summarize(Document[] sourceDocuments, SummarizeOptions options)
```


Generates a summary for an array of documents, with options to adjust the length of the summary.

 **Examples:** 

Shows how to summarize documents with a local model, so the content never leaves the machine.

```

 // Aspose.LLM is a separate package with its own license, for example:
 // new Aspose.LLM.License().SetLicense("Aspose.Total.lic");
 Document firstDoc = new Document(getMyDir() + "Big document.docx");
 Document secondDoc = new Document(getMyDir() + "Document.docx");

 // Disposing the model releases the local model and its native resources.
 AsposeLlmModel model = new AsposeLlmModel("Qwen25_3BPresetCpu");
 SummarizeOptions summarizeOptions = new SummarizeOptions();

 summarizeOptions.setSummaryLength(SummaryLength.SHORT);
 Document summary = model.summarize(firstDoc, summarizeOptions);
 summary.save(getArtifactsDir() + "AI.AsposeLlmSummarize.One.docx");

 summarizeOptions.setSummaryLength(SummaryLength.MEDIUM);
 Document combinedSummary = model.summarize(new Document[] { firstDoc, secondDoc }, summarizeOptions);
 combinedSummary.save(getArtifactsDir() + "AI.AsposeLlmSummarize.Multiple.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) |  |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### translate(Document sourceDocument, int targetLanguage) {#translate-com.aspose.words.Document-int}
```
public Document translate(Document sourceDocument, int targetLanguage)
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
