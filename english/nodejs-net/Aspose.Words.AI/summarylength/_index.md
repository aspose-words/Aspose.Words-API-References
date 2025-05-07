---
title: SummaryLength enumeration
linktitle: SummaryLength enumeration
articleTitle: SummaryLength enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.AI.SummaryLength enumeration. Enumerates possible lengths of summary."
type: docs
weight: 100
url: /nodejs-net/aspose.words.ai/summarylength/
---

## SummaryLength enumeration

Enumerates possible lengths of summary.


### Members

| Name | Description |
| --- | --- |
| VeryShort | Try to generate 1-2 sentences. |
| Short | Try to generate 3-4 sentences. |
| Medium | Try to generate 5-6 sentences. |
| Long | Try to generate 7-10 sentences. |
| VeryLong | Try to generate 11-20 sentences. |

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

