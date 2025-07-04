---
title: AnthropicAiModel.Summarize
linktitle: Summarize
articleTitle: Summarize
second_title: Aspose.Words for .NET
description: Anthropic AI document summarizer with adjustable summary length. Create professional document summaries using Claude AI technology.
type: docs
weight: 10
url: /net/aspose.words.ai/anthropicaimodel/summarize/
---
## Summarize(*[Document](../../../aspose.words/document/), [SummarizeOptions](../../summarizeoptions/)*) {#summarize}

Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected AI model for content processing.

```csharp
public override Document Summarize(Document sourceDocument, SummarizeOptions options = null)
```

| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocument | Document | The document to be summarized. |
| options | SummarizeOptions | Optional settings to control the summary length and other parameters. |

### Return Value

A summarized version of the document's content.

### See Also

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* class [AnthropicAiModel](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)

---

## Summarize(*Document[], [SummarizeOptions](../../summarizeoptions/)*) {#summarize_1}

Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected AI model for processing each document in the array.

```csharp
public override Document Summarize(Document[] sourceDocuments, SummarizeOptions options = null)
```

| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocuments | Document[] | An array of documents to be summarized. |
| options | SummarizeOptions | Optional settings to control the summary length and other parameters |

### Return Value

A summarized version of the document's content.

### See Also

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* class [AnthropicAiModel](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)
