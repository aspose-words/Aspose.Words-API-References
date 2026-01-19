---
title: AiModel class
linktitle: AiModel class
articleTitle: AiModel class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.AI.AiModel class. Represents information about a Generative Language Model."
type: docs
weight: 10
url: /nodejs-net/aspose.words.ai/aimodel/
---

## AiModel class

Represents information about a Generative Language Model.


### Properties

| Name | Description |
| --- | --- |
| [timeout](./timeout/) | Gets or sets the number of milliseconds to wait before the request to AI model times out. The default value is 100,000 milliseconds (100 seconds). |
| [url](./url/) | Gets or sets a URL of the model. The default value is specific for the model. |

### Methods

| Name | Description |
| --- | --- |
|[ asAnthropicAiModel()](./asAnthropicAiModel/#default) |  |
|[ checkGrammar(sourceDocument, options)](./checkGrammar/#document_checkgrammaroptions) | Checks grammar of the provided document. This operation leverages the connected AI model for checking grammar of document. |
|[ create(modelType)](./create/#aimodeltype) | Creates a new instance of [AiModel](./) class. |
|[ createClaude35Haiku()](./createClaude35Haiku/#default) | Creates a new instance of Claude 3.5 Haiku generative model type. |
|[ createClaude35Sonnet()](./createClaude35Sonnet/#default) | Creates a new instance of Claude 3.5 Sonnet generative model type. |
|[ createClaude3Haiku()](./createClaude3Haiku/#default) | Creates a new instance of Claude 3 Haiku generative model type. |
|[ createClaude3Opus()](./createClaude3Opus/#default) | Creates a new instance of Claude 3 Opus generative model type. |
|[ createClaude3Sonnet()](./createClaude3Sonnet/#default) | Creates a new instance of Claude 3 Sonnet generative model type. |
|[ createGemini15Flash()](./createGemini15Flash/#default) | Creates a new instance of Gemini 1.5 Flash generative model type. |
|[ createGemini15Pro()](./createGemini15Pro/#default) | Creates a new instance of Gemini 1.5 Pro generative model type. |
|[ createGpt35Turbo()](./createGpt35Turbo/#default) | Creates a new instance of GPT-3.5 Turbo generative model type. |
|[ createGpt4O()](./createGpt4O/#default) | Creates a new instance of GPT-4o generative model type. |
|[ createGpt4OMini()](./createGpt4OMini/#default) | Creates a new instance of GPT-4 mini generative model type. |
|[ createGpt4Turbo()](./createGpt4Turbo/#default) | Creates a new instance of GPT-4 Turbo generative model type. |
|[ setApiKey(apiKey)](./setApiKey/#string) | Sets a specified API key to the model. |
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

