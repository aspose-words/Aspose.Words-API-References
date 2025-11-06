---
title: AiModel.Url
linktitle: Url
articleTitle: Url
second_title: Aspose.Words for .NET
description: Specifies the AI model endpoint URL in Aspose.Words for accurate connection setup.
type: docs
weight: 30
url: /net/aspose.words.ai/aimodel/url/
---
## AiModel.Url property

Gets or sets a URL of the model. The default value is specific for the model.

```csharp
public abstract string Url { get; set; }
```

## Examples

Shows how to change model default url.

```csharp
string apiKey = Environment.GetEnvironmentVariable("API_KEY");
AiModel model = AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey);
// Default value "https://api.openai.com/".
model.Url = "https://my.a.com/";
```

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

* class [AiModel](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)
