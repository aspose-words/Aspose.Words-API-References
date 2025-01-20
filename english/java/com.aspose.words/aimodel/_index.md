---
title: AiModel
linktitle: AiModel
second_title: Aspose.Words for Java
description: Represents information about a Generative Language Model in Java.
type: docs
weight: 14
url: /java/com.aspose.words/aimodel/
---

**Inheritance:**
java.lang.Object
```
public abstract class AiModel
```

Represents information about a Generative Language Model.

 **Examples:** 

Shows how to summarize text using OpenAI and Google models.

```

 Document firstDoc = new Document(getMyDir() + "Big document.docx");
 Document secondDoc = new Document(getMyDir() + "Document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use OpenAI or Google generative language models.
 IAiModelText model = ((OpenAiModel)AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey)).withOrganization("Organization").withProject("Project");

 SummarizeOptions options = new SummarizeOptions();
 options.setSummaryLength(SummaryLength.SHORT);
 Document oneDocumentSummary = model.summarize(firstDoc, options);
 oneDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.One.docx");

 options = new SummarizeOptions();
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
| [create(int modelType)](#create-int) |  |
| [withApiKey(String apiKey)](#withApiKey-java.lang.String) | Sets a specified API key to the model. |
### AiModel() {#AiModel}
```
public AiModel()
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
 IAiModelText model = ((OpenAiModel)AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey)).withOrganization("Organization").withProject("Project");

 SummarizeOptions options = new SummarizeOptions();
 options.setSummaryLength(SummaryLength.SHORT);
 Document oneDocumentSummary = model.summarize(firstDoc, options);
 oneDocumentSummary.save(getArtifactsDir() + "AI.AiSummarize.One.docx");

 options = new SummarizeOptions();
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
