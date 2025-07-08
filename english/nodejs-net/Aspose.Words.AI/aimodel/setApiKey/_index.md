---
title: AiModel.setApiKey method
linktitle: setApiKey method
articleTitle: setApiKey method
second_title: Aspose.Words for Node.js
description: "AiModel.setApiKey method. Sets a specified API key to the model."
type: docs
weight: 180
url: /nodejs-net/aspose.words.ai/aimodel/setApiKey/
---

## setApiKey(apiKey) {#string}

Sets a specified API key to the model.


```js
setApiKey(apiKey: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| apiKey | string |  |

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

* module [Aspose.Words.AI](../../)
* class [AiModel](../)

