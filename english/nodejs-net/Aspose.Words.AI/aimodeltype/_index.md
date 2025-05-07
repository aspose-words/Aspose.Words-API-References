---
title: AiModelType enumeration
linktitle: AiModelType enumeration
articleTitle: AiModelType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.AI.AiModelType enumeration. Represents the types of [AiModel](../aimodel/) that can be integrated into the document processing workflow."
type: docs
weight: 20
url: /nodejs-net/aspose.words.ai/aimodeltype/
---

## AiModelType enumeration

Represents the types of [AiModel](../aimodel/) that can be integrated into the document processing workflow.


This enumeration is used to define which large language model (LLM) should be utilized for tasks
such as summarization, translation, and content generation.


### Members

| Name | Description |
| --- | --- |
| Gpt4O | GPT-4o generative model type. |
| Gpt4OMini | GPT-4o mini generative model type. |
| Gpt4Turbo | GPT-4 Turbo generative model type. |
| Gpt35Turbo | GPT-3.5 Turbo generative model type. |
| Gemini15Flash | Gemini 1.5 Flash generative model type. |
| Gemini15Flash8B | Gemini 1.5 Flash-8B generative model type. |
| Gemini15Pro | Gemini 1.5 Pro generative model type. |
| Claude35Sonnet | Claude 3.5 Sonnet generative model type. |
| Claude35Haiku | Claude 3.5 Haiku generative model type. |
| Claude3Opus | Claude 3 Opus generative model type. |
| Claude3Sonnet | Claude 3 Sonnet generative model type. |
| Claude3Haiku | Claude 3 Haiku generative model type. |

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

