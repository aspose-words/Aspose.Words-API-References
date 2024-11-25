---
title: OpenAiModel
linktitle: OpenAiModel
second_title: Aspose.Words for Java
description: An abstract class representing the integration with OpenAIs large language models within the Aspose.Words in Java.
type: docs
weight: 481
url: /java/com.aspose.words/openaimodel/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.AiModel](../../com.aspose.words/aimodel/)

**All Implemented Interfaces:**
[com.aspose.words.IAiModelText](../../com.aspose.words/iaimodeltext/)
```
public abstract class OpenAiModel extends AiModel implements IAiModelText
```

An abstract class representing the integration with OpenAI's large language models within the Aspose.Words.

 **Examples:** 

Shows how to summarize text using OpenAI and Google models.

```

 Document firstDoc = new Document(getMyDir() + "Big document.docx");
 Document secondDoc = new Document(getMyDir() + "Document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use OpenAI or Google generative language models.
 IAiModelText model = (IAiModelText)AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);

 Document oneDocumentSummary = model.summarize(firstDoc, new SummarizeOptions(); { oneDocumentSummary.setSummaryLength(SummaryLength.SHORT); });
 oneDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.One.docx");

 Document multiDocumentSummary = model.summarize(new Document[] { firstDoc, secondDoc }, new SummarizeOptions(); { multiDocumentSummary.setSummaryLength(SummaryLength.LONG); });
 multiDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.Multi.docx");
 
```
## Constructors

| Constructor | Description |
| --- | --- |
| [OpenAiModel()](#OpenAiModel) |  |
## Methods

| Method | Description |
| --- | --- |
| [create(int modelType)](#create-int) |  |
| [summarize(Document doc, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) |  |
| [summarize(Document[] docs, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | Sets a specified API key to the model. |
| [withOrganization(String organizationId)](#withOrganization-java.lang.String) | Sets a specified Organization to the model. |
| [withProject(String projectId)](#withProject-java.lang.String) | Sets a specified Project to the model. |
### OpenAiModel() {#OpenAiModel}
```
public OpenAiModel()
```


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
### summarize(Document doc, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public Document summarize(Document doc, SummarizeOptions options)
```


Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected AI model for content processing.

 **Examples:** 

Shows how to summarize text using OpenAI and Google models.

```

 Document firstDoc = new Document(getMyDir() + "Big document.docx");
 Document secondDoc = new Document(getMyDir() + "Document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use OpenAI or Google generative language models.
 IAiModelText model = (IAiModelText)AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);

 Document oneDocumentSummary = model.summarize(firstDoc, new SummarizeOptions(); { oneDocumentSummary.setSummaryLength(SummaryLength.SHORT); });
 oneDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.One.docx");

 Document multiDocumentSummary = model.summarize(new Document[] { firstDoc, secondDoc }, new SummarizeOptions(); { multiDocumentSummary.setSummaryLength(SummaryLength.LONG); });
 multiDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.Multi.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### summarize(Document[] docs, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public Document summarize(Document[] docs, SummarizeOptions options)
```


Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected AI model for processing each document in the array.

 **Examples:** 

Shows how to summarize text using OpenAI and Google models.

```

 Document firstDoc = new Document(getMyDir() + "Big document.docx");
 Document secondDoc = new Document(getMyDir() + "Document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use OpenAI or Google generative language models.
 IAiModelText model = (IAiModelText)AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);

 Document oneDocumentSummary = model.summarize(firstDoc, new SummarizeOptions(); { oneDocumentSummary.setSummaryLength(SummaryLength.SHORT); });
 oneDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.One.docx");

 Document multiDocumentSummary = model.summarize(new Document[] { firstDoc, secondDoc }, new SummarizeOptions(); { multiDocumentSummary.setSummaryLength(SummaryLength.LONG); });
 multiDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.Multi.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| docs | [Document\[\]](../../com.aspose.words/document/) |  |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) |  |

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
 IAiModelText model = (IAiModelText)AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);

 Document oneDocumentSummary = model.summarize(firstDoc, new SummarizeOptions(); { oneDocumentSummary.setSummaryLength(SummaryLength.SHORT); });
 oneDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.One.docx");

 Document multiDocumentSummary = model.summarize(new Document[] { firstDoc, secondDoc }, new SummarizeOptions(); { multiDocumentSummary.setSummaryLength(SummaryLength.LONG); });
 multiDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.Multi.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| apiKey | java.lang.String |  |

**Returns:**
[AiModel](../../com.aspose.words/aimodel/)
### withOrganization(String organizationId) {#withOrganization-java.lang.String}
```
public OpenAiModel withOrganization(String organizationId)
```


Sets a specified Organization to the model.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| organizationId | java.lang.String |  |

**Returns:**
[OpenAiModel](../../com.aspose.words/openaimodel/)
### withProject(String projectId) {#withProject-java.lang.String}
```
public OpenAiModel withProject(String projectId)
```


Sets a specified Project to the model.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| projectId | java.lang.String |  |

**Returns:**
[OpenAiModel](../../com.aspose.words/openaimodel/)
