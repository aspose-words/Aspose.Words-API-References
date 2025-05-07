---
title: IAiModelText class
linktitle: IAiModelText class
articleTitle: IAiModelText class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.AI.IAiModelText class. The common interface for AI models designed to generate a variety of text-based content."
type: docs
weight: 60
url: /nodejs-net/aspose.words.ai/iaimodeltext/
---

## IAiModelText class

The common interface for AI models designed to generate a variety of text-based content.


### Methods

| Name | Description |
| --- | --- |
|[ checkGrammar(sourceDocument, options)](./checkGrammar/#document_checkgrammaroptions) | Checks grammar of the provided document. This operation leverages the connected AI model for checking grammar of document. |
|[ summarize(sourceDocument, options)](./summarize/#document_summarizeoptions) | Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected AI model for content processing. |
|[ summarize(sourceDocuments, options)](./summarize/#document[]_summarizeoptions) | Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected AI model for processing each document in the array. |
|[ translate(sourceDocument, targetLanguage)](./translate/#document_language) | Translates the provided document into the specified target language. This operation leverages the connected AI model for content translating. |

### Examples

Shows how to summarize text using OpenAI and Google models.

```js
let firstDoc = new aw.Document(base.myDir + "Big document.docx");
let secondDoc = new aw.Document(base.myDir + "Document.docx");

const apiKey = process.env.API_KEY;
if (!apiKey) {
  console.warn("API_KEY environment variable is not set.");
  return;
}

// Use OpenAI or Google generative language models.
let model = aw.AI.AiModel.createGpt4OMini();
model.setApiKey(apiKey);
model.setOrganization("Organization");
model.setProject("Project");

let options = new aw.AI.SummarizeOptions();

options.summaryLength = aw.AI.SummaryLength.Short;
let oneDocumentSummary = model.summarize(firstDoc, options);
oneDocumentSummary.save(base.artifactsDir + "AI.AiSummarize.one.docx");

options.summaryLength = aw.AI.SummaryLength.Long;
let multiDocumentSummary = model.summarize([firstDoc, secondDoc], options);
multiDocumentSummary.save(base.artifactsDir + "AI.AiSummarize.multi.docx");
```

### See Also

* module [Aspose.Words.AI](../)

