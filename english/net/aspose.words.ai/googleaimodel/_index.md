---
title: GoogleAiModel Class
linktitle: GoogleAiModel
articleTitle: GoogleAiModel
second_title: Aspose.Words for .NET
description: Aspose.Words.AI.GoogleAiModel class. An abstract class representing the integration with Googles AI models within the Aspose.Words in C#.
type: docs
weight: 40
url: /net/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class

An abstract class representing the integration with Google’s AI models within the Aspose.Words.

```csharp
public abstract class GoogleAiModel : AiModel, IAiModelText
```

## Methods

| Name | Description |
| --- | --- |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Sets a specified API key to the model. |

## Examples

Shows how to summarize text using OpenAI and Google models.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Use OpenAI or Google generative language models.
IAiModelText model = (IAiModelText)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey);

Document oneDocumentSummary = model.Summarize(firstDoc, new SummarizeOptions() { SummaryLength = SummaryLength.Short });
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, new SummarizeOptions() { SummaryLength = SummaryLength.Long });
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### See Also

* class [AiModel](../aimodel/)
* interface [IAiModelText](../iaimodeltext/)
* namespace [Aspose.Words.AI](../../aspose.words.ai/)
* assembly [Aspose.Words](../../)
