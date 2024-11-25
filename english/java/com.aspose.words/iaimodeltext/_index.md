---
title: IAiModelText
linktitle: IAiModelText
second_title: Aspose.Words for Java
description: The common interface for AI models designed to generate a variety of text-based content in Java.
type: docs
weight: 707
url: /java/com.aspose.words/iaimodeltext/
---
```
public interface IAiModelText
```

The common interface for AI models designed to generate a variety of text-based content.

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
## Methods

| Method | Description |
| --- | --- |
| [summarize(Document doc, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Generates a summary of the specified document, with options to adjust the length of the summary. |
| [summarize(Document[] docs, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Generates summaries for an array of documents, with options to control the summary length and other settings. |
### summarize(Document doc, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document doc, SummarizeOptions options)
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
| doc | [Document](../../com.aspose.words/document/) | The document to be summarized. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Optional settings to control the summary length and other parameters. |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] docs, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document[] docs, SummarizeOptions options)
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
| docs | [Document\[\]](../../com.aspose.words/document/) | An array of documents to be summarized. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Optional settings to control the summary length and other parameters |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
