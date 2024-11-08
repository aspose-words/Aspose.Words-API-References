---
title: IAiModelText.Summarize
linktitle: Summarize
articleTitle: Summarize
second_title: Aspose.Words for .NET
description: IAiModelText Summarize method. Generates a summary of the specified document with options to adjust the length of the summary. This operation leverages the connected AI model for content processing in C#.
type: docs
weight: 10
url: /net/aspose.words.ai/iaimodeltext/summarize/
---
## Summarize(*[Document](../../../aspose.words/document/), [SummarizeOptions](../../summarizeoptions/)*) {#summarize}

Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected AI model for content processing.

```csharp
public Document Summarize(Document doc, SummarizeOptions options = null)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | Document | The document to be summarized. |
| options | SummarizeOptions | Optional settings to control the summary length and other parameters. |

### Return Value

A summarized version of the document's content.

## Examples

Shows how to summarize text using OpenAI and Google models.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Use OpenAI or Google generative language models.
IAiModelText model = (IAiModelText)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey);

Document oneDocumentSummary = model.Summarize(firstDoc, new SummarizeOptions() { SummaryLength = SummaryLength.Short });
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, new SummarizeOptions() { SummaryLength = SummaryLength.Long });
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### See Also

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)

---

## Summarize(*Document[], [SummarizeOptions](../../summarizeoptions/)*) {#summarize_1}

Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected AI model for processing each document in the array.

```csharp
public Document Summarize(Document[] docs, SummarizeOptions options = null)
```

| Parameter | Type | Description |
| --- | --- | --- |
| docs | Document[] | An array of documents to be summarized. |
| options | SummarizeOptions | Optional settings to control the summary length and other parameters |

### Return Value

A summarized version of the document's content.

## Examples

Shows how to summarize text using OpenAI and Google models.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Use OpenAI or Google generative language models.
IAiModelText model = (IAiModelText)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey);

Document oneDocumentSummary = model.Summarize(firstDoc, new SummarizeOptions() { SummaryLength = SummaryLength.Short });
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, new SummarizeOptions() { SummaryLength = SummaryLength.Long });
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### See Also

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* interface [IAiModelText](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)
