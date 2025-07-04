---
title: AiModel.CheckGrammar
linktitle: CheckGrammar
articleTitle: CheckGrammar
second_title: Aspose.Words for .NET
description: AI-powered grammar checker API for documents. Automatically detect and fix grammar errors in Word files using advanced language models.
type: docs
weight: 20
url: /net/aspose.words.ai/aimodel/checkgrammar/
---
## AiModel.CheckGrammar method

Checks grammar of the provided document. This operation leverages the connected AI model for checking grammar of document.

```csharp
public virtual Document CheckGrammar(Document sourceDocument, CheckGrammarOptions options = null)
```

| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocument | Document | The document being checked for grammar. |
| options | CheckGrammarOptions | Optional settings to control how grammar will be checked. |

### Return Value

A new [`Document`](../../../aspose.words/document/) with checked grammar.

## Examples

Shows how to check the grammar of a document.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Use OpenAI generative language models.
AiModel model = AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey);

CheckGrammarOptions grammarOptions = new CheckGrammarOptions();
grammarOptions.ImproveStylistics = true;

Document proofedDoc = model.CheckGrammar(doc, grammarOptions);
proofedDoc.Save(ArtifactsDir + "AI.AiGrammar.docx");
```

### See Also

* class [Document](../../../aspose.words/document/)
* class [CheckGrammarOptions](../../checkgrammaroptions/)
* class [AiModel](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)
