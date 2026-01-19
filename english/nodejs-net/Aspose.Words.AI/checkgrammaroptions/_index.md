---
title: CheckGrammarOptions class
linktitle: CheckGrammarOptions class
articleTitle: CheckGrammarOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.AI.CheckGrammarOptions class. Allows to specify various options while checking grammar of a document using AI."
type: docs
weight: 40
url: /nodejs-net/aspose.words.ai/checkgrammaroptions/
---

## CheckGrammarOptions class

Allows to specify various options while checking grammar of a document using AI.


### Constructors
| Name | Description |
| --- | --- |
| [CheckGrammarOptions()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [improveStylistics](./improveStylistics/) | Allows to specify either AI will try to improve stylistics of the text being proofed. Default value is ``false``. |
| [makeRevisions](./makeRevisions/) | Allows to specify either final or revised document to be returned with proofed text. Default value is ``false``. |
| [preserveFormatting](./preserveFormatting/) | Allows to specify either [AiModel.checkGrammar()](../aimodel/checkGrammar/#document_checkgrammaroptions) will try to preserve layout and formatting of the original document, or not. Default value is ``true``. |

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

* module [Aspose.Words.AI](../)

