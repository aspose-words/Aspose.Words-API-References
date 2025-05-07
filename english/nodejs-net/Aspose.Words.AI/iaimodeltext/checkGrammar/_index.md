---
title: IAiModelText.checkGrammar method
linktitle: checkGrammar method
articleTitle: checkGrammar method
second_title: Aspose.Words for Node.js
description: "IAiModelText.checkGrammar method. Checks grammar of the provided document"
type: docs
weight: 10
url: /nodejs-net/aspose.words.ai/iaimodeltext/checkGrammar/
---

## checkGrammar(sourceDocument, options) {#document_checkgrammaroptions}

Checks grammar of the provided document.
This operation leverages the connected AI model for checking grammar of document.


```js
checkGrammar(sourceDocument: Aspose.Words.Document, options: Aspose.Words.AI.CheckGrammarOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocument | [Document](../../../aspose.words/document/) | The document being checked for grammar. |
| options | [CheckGrammarOptions](../../checkgrammaroptions/) | Optional settings to control how grammar will be checked. |

### Returns

A new [Document](../../../aspose.words/document/) with checked grammar.


### Examples

Shows how to check the grammar of a document.

```js
let doc = new aw.Document(base.myDir + "Big document.docx");

const apiKey = process.env.API_KEY;
if (!apiKey) {
  console.warn("API_KEY environment variable is not set.");
  return;
}

// Use OpenAI generative language models.
let model = aw.AI.AiModel.createGpt4OMini();
model.setApiKey(apiKey);

let grammarOptions = new aw.AI.CheckGrammarOptions();
grammarOptions.improveStylistics = true;

let proofedDoc = model.checkGrammar(doc, grammarOptions);
proofedDoc.save(base.artifactsDir + "AI.AiGrammar.docx");
```

### See Also

* module [Aspose.Words.AI](../../)
* class [IAiModelText](../)

