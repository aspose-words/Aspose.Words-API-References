---
title: SummarizeOptions class
linktitle: SummarizeOptions class
articleTitle: SummarizeOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.AI.SummarizeOptions class. Allows to specify various options for summarizing document content."
type: docs
weight: 80
url: /nodejs-net/aspose.words.ai/summarizeoptions/
---

## SummarizeOptions class

Allows to specify various options for summarizing document content.


### Constructors
| Name | Description |
| --- | --- |
| [SummarizeOptions()](./constructor/#default) | Initializes a new instances of [SummarizeOptions](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [summaryLength](./summaryLength/) | Allows to specify summary length. Default value is [SummaryLength.Medium](../summarylength/#Medium). |

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

