---
title: IAiModelText.summarize method
linktitle: summarize method
articleTitle: summarize method
second_title: Aspose.Words for Python
description: "aspose.words.ai.IAiModelText.summarize method"
type: docs
weight: 20
url: /python-net/aspose.words.ai/iaimodeltext/summarize/
---

## summarize(source_document, options) {#document_summarizeoptions}

Generates a summary of the specified document, with options to adjust the length of the summary.
This operation leverages the connected AI model for content processing.


```python
def summarize(self, source_document: aspose.words.Document, options: aspose.words.ai.SummarizeOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| source_document | [Document](../../../aspose.words/document/) | The document to be summarized. |
| options | [SummarizeOptions](../../summarizeoptions/) | Optional settings to control the summary length and other parameters. |

### Returns

A summarized version of the document's content.


## summarize(source_documents, options) {#documentlist_summarizeoptions}

Generates summaries for an array of documents, with options to control the summary length and other settings.
This method utilizes the connected AI model for processing each document in the array.


```python
def summarize(self, source_documents: List[aspose.words.Document], options: aspose.words.ai.SummarizeOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| source_documents | List[[Document](../../../aspose.words/document/)] | An array of documents to be summarized. |
| options | [SummarizeOptions](../../summarizeoptions/) | Optional settings to control the summary length and other parameters |

### Returns

A summarized version of the document's content.


## See Also

* module [aspose.words.ai](../../)
* class [IAiModelText](../)

