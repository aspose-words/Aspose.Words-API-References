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

Shows how to use self-hosted AI model based on OpenAiModel.

```csharp
public void SelfHostedModel()
{
    Document doc = new Document(MyDir + "Big document.docx");

    string apiKey = Environment.GetEnvironmentVariable("API_KEY");
    // Use OpenAI generative language models.
    AiModel model = new CustomAiModel().WithApiKey(apiKey);
    model.Url = "https://my.a.com/";

    Document translatedDoc = model.Translate(doc, Language.Russian);
    translatedDoc.Save(ArtifactsDir + "AI.SelfHostedModel.docx");
}

/// <summary>
/// Custom self-hosted AI model.
/// </summary>
internal class CustomAiModel : OpenAiModel
{
    /// <summary>
    /// Gets model name.
    /// </summary>
    protected override string Name
    {
        get { return "my-model-24b"; }
    }
}
```

### See Also

* class [AiModel](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)
