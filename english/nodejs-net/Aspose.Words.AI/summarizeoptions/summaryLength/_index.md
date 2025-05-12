---
title: SummarizeOptions.summaryLength property
linktitle: summaryLength property
articleTitle: summaryLength property
second_title: Aspose.Words for Node.js
description: "SummarizeOptions.summaryLength property. Allows to specify summary length"
type: docs
weight: 20
url: /nodejs-net/aspose.words.ai/summarizeoptions/summaryLength/
---

## SummarizeOptions.summaryLength property

Allows to specify summary length.
Default value is [SummaryLength.Medium](../../summarylength/#Medium).



```js
get summaryLength(): Aspose.Words.AI.SummaryLength
```

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
* class [SummarizeOptions](../)

