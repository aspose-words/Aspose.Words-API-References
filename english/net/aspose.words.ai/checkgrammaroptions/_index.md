---
title: CheckGrammarOptions Class
linktitle: CheckGrammarOptions
articleTitle: CheckGrammarOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.AI.CheckGrammarOptions class. Allows to specify various options while checking grammar of a document using AI in C#.
type: docs
weight: 40
url: /net/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class

Allows to specify various options while checking grammar of a document using AI.

```csharp
public class CheckGrammarOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [CheckGrammarOptions](checkgrammaroptions/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [ImproveStylistics](../../aspose.words.ai/checkgrammaroptions/improvestylistics/) { get; set; } | Allows to specify either AI will try to improve stylistics of the text being proofed. Default value is `false`. |
| [MakeRevisions](../../aspose.words.ai/checkgrammaroptions/makerevisions/) { get; set; } | Allows to specify either final or revised document to be returned with proofed text. Default value is `false`. |
| [PreserveFormatting](../../aspose.words.ai/checkgrammaroptions/preserveformatting/) { get; set; } | Allows to specify either [`CheckGrammar`](../iaimodeltext/checkgrammar/) will try to preserve layout and formatting of the original document, or not. Default value is `true`. |

## Examples

Shows how to check the grammar of a document.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Use OpenAI generative language models.
IAiModelText model = (IAiModelText)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey);

CheckGrammarOptions grammarOptions = new CheckGrammarOptions();
grammarOptions.ImproveStylistics = true;

Document proofedDoc = model.CheckGrammar(doc, grammarOptions);
proofedDoc.Save("AI.AiGrammar.docx");
```

### See Also

* namespace [Aspose.Words.AI](../../aspose.words.ai/)
* assembly [Aspose.Words](../../)
