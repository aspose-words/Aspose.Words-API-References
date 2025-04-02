---
title: IAiModelText.summarize method
linktitle: summarize method
articleTitle: summarize method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.AI.IAiModelText.summarize method"
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.AI/iaimodeltext/summarize/
---

## summarize(sourceDocument, options) {#document_summarizeoptions}

Generates a summary of the specified document, with options to adjust the length of the summary.
This operation leverages the connected AI model for content processing.


```js
summarize(sourceDocument: Aspose.Words.Documentoptions: Aspose.Words.AI.SummarizeOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocument | [Document](../../../Aspose.Words/document/) | The document to be summarized. |
| options | [SummarizeOptions](../../summarizeoptions/) | Optional settings to control the summary length and other parameters. |

### Returns

A summarized version of the document's content.


## summarize(sourceDocuments, options) {#document[]_summarizeoptions}

Generates summaries for an array of documents, with options to control the summary length and other settings.
This method utilizes the connected AI model for processing each document in the array.


```js
summarize(sourceDocuments: Aspose.Words.Document[]options: Aspose.Words.AI.SummarizeOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocuments | [Document](../../../Aspose.Words/document/)[] | An array of documents to be summarized. |
| options | [SummarizeOptions](../../summarizeoptions/) | Optional settings to control the summary length and other parameters |

### Returns

A summarized version of the document's content.


## See Also

* module [Aspose.Words.AI](../../)
* class [IAiModelText](../)

