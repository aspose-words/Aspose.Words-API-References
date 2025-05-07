---
title: OpenAiModel class
linktitle: OpenAiModel class
articleTitle: OpenAiModel class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.AI.OpenAiModel class. An abstract class representing the integration with OpenAI's large language models within the Aspose.Words."
type: docs
weight: 80
url: /nodejs-net/aspose.words.ai/openaimodel/
---

## OpenAiModel class

An abstract class representing the integration with OpenAI's large language models within the Aspose.Words.


**Inheritance:** [OpenAiModel](./) → [AiModel](../aimodel/)

### Methods

| Name | Description |
| --- | --- |
|[ asAnthropicAiModel()](../aimodel/asAnthropicAiModel/#default) | Cast AiModel to [AnthropicAiModel](../anthropicaimodel/).<br>(Inherited from [AiModel](../aimodel/)) |
|[ asGoogleAiModel()](../aimodel/asGoogleAiModel/#default) | Cast AiModel to [GoogleAiModel](../googleaimodel/).<br>(Inherited from [AiModel](../aimodel/)) |
|[ asOpenAiModel()](../aimodel/asOpenAiModel/#default) | Cast AiModel to [OpenAiModel](./).<br>(Inherited from [AiModel](../aimodel/)) |
|[ checkGrammar(doc, options)](./checkGrammar/#document_checkgrammaroptions) | Checks grammar of the provided document. |
|[ create(modelType)](../aimodel/create/#aimodeltype) | Creates a new instance of [AiModel](../aimodel/) class.<br>(Inherited from [AiModel](../aimodel/)) |
|[ createClaude35Haiku()](../aimodel/createClaude35Haiku/#default) | Creates a new instance of Claude 3.5 Haiku generative model type.<br>(Inherited from [AiModel](../aimodel/)) |
|[ createClaude35Sonnet()](../aimodel/createClaude35Sonnet/#default) | Creates a new instance of Claude 3.5 Sonnet generative model type.<br>(Inherited from [AiModel](../aimodel/)) |
|[ createClaude3Haiku()](../aimodel/createClaude3Haiku/#default) | Creates a new instance of Claude 3 Haiku generative model type.<br>(Inherited from [AiModel](../aimodel/)) |
|[ createClaude3Opus()](../aimodel/createClaude3Opus/#default) | Creates a new instance of Claude 3 Opus generative model type.<br>(Inherited from [AiModel](../aimodel/)) |
|[ createClaude3Sonnet()](../aimodel/createClaude3Sonnet/#default) | Creates a new instance of Claude 3 Sonnet generative model type.<br>(Inherited from [AiModel](../aimodel/)) |
|[ createGemini15Flash()](../aimodel/createGemini15Flash/#default) | Creates a new instance of Gemini 1.5 Flash generative model type.<br>(Inherited from [AiModel](../aimodel/)) |
|[ createGemini15Flash8B()](../aimodel/createGemini15Flash8B/#default) | Creates a new instance of Gemini 1.5 Flash-8B generative model type.<br>(Inherited from [AiModel](../aimodel/)) |
|[ createGemini15Pro()](../aimodel/createGemini15Pro/#default) | Creates a new instance of Gemini 1.5 Pro generative model type.<br>(Inherited from [AiModel](../aimodel/)) |
|[ createGpt35Turbo()](../aimodel/createGpt35Turbo/#default) | Creates a new instance of GPT-3.5 Turbo generative model type.<br>(Inherited from [AiModel](../aimodel/)) |
|[ createGpt4O()](../aimodel/createGpt4O/#default) | Creates a new instance of GPT-4o generative model type.<br>(Inherited from [AiModel](../aimodel/)) |
|[ createGpt4OMini()](../aimodel/createGpt4OMini/#default) | Creates a new instance of GPT-4 mini generative model type.<br>(Inherited from [AiModel](../aimodel/)) |
|[ createGpt4Turbo()](../aimodel/createGpt4Turbo/#default) | Creates a new instance of GPT-4 Turbo generative model type.<br>(Inherited from [AiModel](../aimodel/)) |
|[ setApiKey(apiKey)](../aimodel/setApiKey/#string) | Sets a specified API key to the model.<br>(Inherited from [AiModel](../aimodel/)) |
|[ setOrganization(organizationId)](./setOrganization/#string) | Sets a specified Organization to the model. |
|[ setProject(projectId)](./setProject/#string) | Sets a specified Project to the model. |
|[ summarize(doc, options)](./summarize/#document_summarizeoptions) | Summarizes specified [Document](../../aspose.words/document/) object. |
|[ summarize(docs, options)](./summarize/#document[]_summarizeoptions) | Summarizes specified [Document](../../aspose.words/document/) objects. |
|[ translate(doc, language)](./translate/#document_language) | Translates specified [Document](../../aspose.words/document/) objects. |

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
* class [AiModel](../aimodel/)

