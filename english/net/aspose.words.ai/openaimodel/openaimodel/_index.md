---
title: OpenAiModel
linktitle: OpenAiModel
articleTitle: OpenAiModel
second_title: Aspose.Words for .NET
description: Initialize the OpenAiModel in Aspose.Words AI to connect OpenAI models and enable AI-powered document processing and automation.
type: docs
weight: 10
url: /net/aspose.words.ai/openaimodel/openaimodel/
---
## OpenAiModel(*string, string*) {#constructor_1}

Initializes a new instance of [`OpenAiModel`](../) class.

```csharp
public OpenAiModel(string name, string apiKey)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | The name of the model. For example, gpt-5.2-chat-latest. |
| apiKey | String | The API key to use the OpenAi API. |

## Examples

Shows how to create an OpenAI model instance directly using an API key and model name.

```csharp
string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Create an OpenAI model instance using the constructor with model name and API key.
OpenAiModel model = new OpenAiModel("gpt-4o-mini", apiKey);

Document doc = new Document(MyDir + "Big document.docx");
// Summarize the document using the OpenAI model with short summary length.
SummarizeOptions summarizeOptions = new SummarizeOptions() { SummaryLength = SummaryLength.VeryShort };
Document summary = model.Summarize(doc, summarizeOptions);

summary.Save(ArtifactsDir + "OpenAiModel.OpenAiModelConstructor.docx");
```

### See Also

* class [OpenAiModel](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)

---

## OpenAiModel(*string*) {#constructor}

Initializes a new instance of [`OpenAiModel`](../) class.

```csharp
public OpenAiModel(string name)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | The name of the model. For example, gpt-5.2-chat-latest. |

### See Also

* class [OpenAiModel](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)
