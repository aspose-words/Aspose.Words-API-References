---
title: AiModel.create method
linktitle: create method
articleTitle: create method
second_title: Aspose.Words for Node.js
description: "AiModel.create method. Creates a new instance of [AiModel](../) class."
type: docs
weight: 50
url: /nodejs-net/aspose.words.ai/aimodel/create/
---

## create(modelType) {#aimodeltype}

Creates a new instance of [AiModel](../) class.



```js
create(modelType: Aspose.Words.AI.AiModelType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| modelType | [AiModelType](../../aimodeltype/) |  |

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

